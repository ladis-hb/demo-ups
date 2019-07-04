<template>
    <el-row :gutter="12">
      <el-col :span="12">
          <!-- -->
            <el-card shadow="always" id="zs" style="height:300px"></el-card>
            
      </el-col>
      <el-col :span="12">
            <el-card shadow="always">
                zsxs
            </el-card>
      </el-col>
    </el-row>
</template>

<script>
import echart from 'echarts'

export default {
    name:'emain',
    data(){
        return{
            charts:category
        }
    },

    mounted(){
        this.chart(document.getElementById('zs'),this.charts)
    },

    methods:{
        chart(id,charts){
            echart.init(id)
            .setOption(charts)
        }
    }

    
}

//饼图
var pie = {
        title:{
            txet:'南丁格尔',
            subtext:'测试'
        },
        backgroundColor: '#2c343c',
        series : [
          {
            name: '访问来源',
            type: 'pie',
            radius: '55%',
            data:[
                {value:235, name:'视频广告'},
                {value:274, name:'联盟广告'},
                {value:310, name:'邮件营销'},
                {value:335, name:'直接访问'},
                {value:400, name:'搜索引擎'}
            ],
            roseType: 'angle',
            label: {
                normal: {
                    textStyle: {
                        color: 'rgba(255, 255, 255, 0.3)'
                    }
                }
            },
            labelLine: {
                normal: {
                    lineStyle: {
                        color: 'rgba(255, 255, 255, 0.3)'
                    }
                }
            },
            itemStyle: {
                normal: {
                    shadowBlur: 200,
                    shadowColor: 'rgba(0, 0, 0, 0.5)'
                }
            }
          }
        ]
    };

//折线图
var category = {
    title: {
        text: ''
    },
    tooltip: {
        trigger: 'axis'
    },
    legend: {
        data:['邮件营销','联盟广告','视频广告','直接访问','搜索引擎']
    },
    grid: {
        left: '3%',
        right: '4%',
        bottom: '3%',
        containLabel: true
    },
    toolbox: {
        feature: {
            saveAsImage: {}
        }
    },
    xAxis: {
        type: 'category',
        boundaryGap: false,
        data: ['周一','周二','周三','周四','周五','周六','周日']
    },
    yAxis: {
        type: 'value'
    },
    series: [
        {
            name:'邮件营销',
            type:'line',
            stack: '总量',
            data:[120, 132, 101, 134, 90, 230, 210]
        },
        {
            name:'联盟广告',
            type:'line',
            stack: '总量',
            data:[220, 182, 191, 234, 290, 330, 310]
        },
        {
            name:'视频广告',
            type:'line',
            stack: '总量',
            data:[150, 232, 201, 154, 190, 330, 410]
        },
        {
            name:'直接访问',
            type:'line',
            stack: '总量',
            data:[320, 332, 301, 334, 390, 330, 320]
        },
        {
            name:'搜索引擎',
            type:'line',
            stack: '总量',
            data:[820, 932, 901, 934, 1290, 1330, 1320]
        }
    ]
};

</script>
