# expandableadapter



继承自 RecyclerView.Adapter，支持header，child, group, groupchild, footer 分组,并且支持group悬浮效果(Sticky效果).



![image](https://github.com/qbaowei/ExpandableAdapter/raw/master/screenshots/ExpandableAdapter.gif)


#使用说明


1.需要Group悬浮,将RecyclerView包裹在'StickyLayout'里面,并且调用'stickylayout'的init函数传入参数true(true,表示group悬浮,false表示不悬浮)，同时Adapter要实现StickyListener


    <com.qbw.recyclerview.expandable.StickyLayout
        android:id="@+id/stickylayout"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <android.support.v7.widget.RecyclerView
            android:id="@+id/recyclerview"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />
    </com.qbw.recyclerview.expandable.StickyLayout>


2.不需要Group悬浮,可直接使用'RecyclerView'


    <android.support.v7.widget.RecyclerView
            android:id="@+id/recyclerview"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />



# Download


Gradle:

compile 'com.qbw.recyclerview:expandableadapter:3.2.0'


# v3.2.0

1.构造函数参数去掉Context（如果需要，添加到自己的Adapter基类中）

2.添加回调函数返回StickyGroupViewHolder的水平margin值

3.优化convertXXXPosition函数

# v3.1.0

1.将StickyLayout需要的回调抽离成独立的一个StickyListener

2.优化getXXXPosition函数

# v3.0.0

1.重写group悬浮逻辑

2.修复v2.9.0bug

# v2.10.0

1.addGroup(int, T)增加返回值，返回实际group插入的位置


# v2.9.0

1.增加addGroup(int, T)将group插入指定的位置

已知影响：addGroup(int, T)会导致group悬浮有问题


# v2.8.1


1.修复Group没有child时无法删除Group


# v2.8.0


1.增加clearChild(beginPos)


# v2.7.1


1.clearGroupChild,bug修复


# Author:


qbaowei@qq.com

