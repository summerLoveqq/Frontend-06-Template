学习笔记

1 sorted抽象类
    自定义 compare 方法，给类添加push、get方法，实现数组数据按照自定义顺序取出。
2 A*寻路算法原理
    a. 从起点 start 开始，初始化queue队列；
    b. 查看 start 相邻的方格，如果是障碍物或者已经在queue中，则忽略，否则，把他们push到queue中。把起点 start 设置为这些点的父节点；
    c. 把 start 从 queue 中移除，加入到 table(后面获取路径使用) 中；
    d. 继续从queue中取出一个点（I: 按照最短路径的distance方式的顺序取出），作为新的start，重复上述操作，直到找到end 或 没有新的点为止；
    e. 如果没有找到新的点，返回null，表示两点直接不存在路径；
       否则，从table里逐次取出数据，最后返回路径；
    注释：I中的计算方式有优化空间，短期实在没时间研究，给自己记一个todo项，后面完善；
    extends: 在网上搜索的时候发现了一个为B*算法的寻路，简单看了下，觉得有点问题，再记一个todo，后面review的时候自己研究下（https://blog.csdn.net/y13156556538/article/details/70154434?utm_medium=distribute.pc_relevant_download.none-task-blog-baidujs-1.nonecase&depth_1-utm_source=distribute.pc_relevant_download.none-task-blog-baidujs-1.nonecase）；
