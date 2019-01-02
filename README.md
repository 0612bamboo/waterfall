瀑布流新闻网站

预览地址:由于购买的新域名还在解析中，暂无预览地址

瀑布流原理：

重点是图片宽度都一样，当图片加载之后，通过查找图像高度最低的那一列，通过绝对定位设置图片位置

1、设置两个变量，变量colHeightArray每一列图片的高度，变量colCount 每一行放图片的数量

2、用容器的宽度除以img的outerWidth(true)，通过for循环初始化colHeightArray

3、当图片加载之后，遍历colheightarray数组，查找数组中高度最低的那一列，并获取行数和列数

4、通过绝对定位设置图片位置，并更新colHeightArray图片的列高度

实现原理

getData函数：发送ajax每次获取perPageCount条（这里设置是10条）数据，获取次数用curPage计算
getnode函数：把每次获取的10条数据，拼装成jquery对象$node
waterFallPlace函数：把每次获取并显示页面10条的数据按照瀑布流的方式排列

两次状态判断：
1、 isDataArrive让发送数据过程，不能重复发送
2、 isVisible判断元素是否到底了
