# B树
 介绍： http://blog.jobbole.com/79311/  <br>
 b树实现：https://www.jianshu.com/p/d2d1181aa93d

##特点<br>
1. 根节点至少两个子节点
2. 每个节点有M-1个key,升序
3. 位于M-1和M key的子节点的值位于M-1和M key对应的value直接
4. 其他节点至少M/2个子节点


下面是往B树中依次插入
6 10 4 14 5 11 15 3 2 12 1 7 8 8 6 3 6 21 5 15 15 6 32 23 45 65 7 8 6 5 4

![Alt text](./btree.gif)

# B+树

## 特点

1. 有k个子节点的节点有k个key
2. 非叶节点仅具有索引作用，跟记录有关的信息均存放在叶节点
3. 树的所有叶节点构成一个有序链表，可以按照key排序的次序遍历全部记录

![Alt text](./b+tree.gif)

## b+树优点
* 内部节点不包含数据，内存可以存放更多key
* 叶子节点相连，线性遍历较便利