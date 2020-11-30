学习笔记
range
    创建range：document.createRange();
    选择节点：
        range.selectNode() - 选择整个节点，包含子节点；
        selectNodeContents() - 选择节点的子节点；
    setStart() setEnd():
        接受两个参数，参照节点以及几点偏移量；
    操作节点：
        deleteContents() 这个方法能够从文档中删除范围所包含的内容；
        extractContents() 删除并返回文档片段；
        CloneContents() 创建范围对象的一个副本，不会影响原来的节点；
        insertNode() 向范围选区的开始出插入一个节点；
        surroundContents() 环绕范围插入内容；

selectStart事件
    选择文本节点事件