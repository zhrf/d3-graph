# d3-graph 
### d3力学导向图
  * d3.layout.force() 力学图（也称为导向图，也有叫网络拓补图的，反正就是通过排斥得到关系远近的结构）在社交网络研究、信息传播途径等群体关系研究中应用非常广泛，它可以直观地反映群体与群体之间联系的渠道、交集多少，群体内部成员的联系强度等。
详细api请参照官方网站
------
### 参数配置
配置项：

    SVG_WIDTH : 800,            svg元素宽度
            SVG_HEIGHT: 800,            svg元素高度
            IMG_WIDTH :80,              图片宽度
            IMG_HEIGHT:80,              图片高度  
            NODE_CIRCLE_RADIUS : {      圆圈节点半径 适应不同群体
                    0 : 33 ,
                    1 : 28 ,
                    2 : 22
                },
            NODE_CIRCLE_BORDER : {      圆圈节点边距 适应不同群体
                    0 : '#C81B5A',
                    1 : '#456FB4' ,
                    2 : '#363636'
            },
            LINE_COLOR : {              连接线颜色 适应不同群体
                    0 : '#C81B5A',
                    1 : '#456FB4',
                    2 : '#363636',
                }
### 入口数据:
    @param {Object} data 数据来源
                {Array} nodes 节点数据
                    {String} name  节点名称
                    {String} img   节点图片地址
                    {String} group 群组（一级、二级等）
                    {String} type  分类（账号或文章等、可根据需求增加）
                {Array} links 连接来源数据
                    {String} source 起止点  
                    {String} target 起止点 
                    {String} relation 关系类型 
