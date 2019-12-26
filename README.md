# Learning-Python
记录学习Python的笔记
[二级标题1]（##二级标题1）
[二级标题2]（#二级标题2）
#顺序（线性）
def sequential_search(lis,key):
    flag=0
    for i in range(len(lis)):
        if lis[i]==key:
            flag=1
            res=i+1   #下标从0开始，故找到的是第i+1个数
            break
    if flag:
        return res
    else:
        return False
    
if __name__=='__main__':
    LIST= [1, 5, 8, 123, 22, 54, 7, 99, 300, 222]
    print(sequential_search(LIST, 8))

二分查找原理如下：
  二分查找的表必须按照关键字大小有序排列，且采用顺序存储结构。在升序排列的表中，首先将表中间位置的数据与关键字对比，若相等则查找成功
  否则利用中间字将表分为前后两个子表。若关键字小，那么查找前子表；若关键字大，则查找后子表。重复步骤直至找到或子表不存在。
#二分
def bin_search(lis, key):    
    low = 0                         # 最小数下标    
    high = len(lis) - 1       # 最大数下标    
    while low <= high:        
        mid = (low + high) // 2     # 中间数下标        
        if lis[mid] == key:   # 如果中间数下标等于key, 返回            
            return mid        
        elif lis[mid] > key:  # 如果key在中间数左边, 移动high下标            
            high = mid - 1        
        else:                       # 如果key在中间数右边, 移动low下标            
            low = mid + 1    
    return False        # val不存在, 返回False
##二级标题1
常用的算法有一下五种
- 穷举法 - 又称为暴力破解法，对所有的可能性进行验证，直到找到正确答案。
- 贪婪法 - 在对问题求解时，总是做出在当前看来是最好的选择，不追求最优解，快速找到满意解。
- 分治法 - 把一个复杂的问题分成两个或更多的相同或相似的子问题，再把子问题分成更小的子问题，直到可以直接求解的程度，最后将子问题的解进行合并得到原问题的解。
- 回溯法 - 回溯法又称为试探法，按选优条件向前搜索，当搜索到某一步发现原先选择并不优或达不到目标时，就退回一步重新选择。
- 动态规划 - 基本思想也是将待求解问题分解成若干个子问题，先求解并保存这些子问题的解，避免产生大量的重复运算。
##二级标题2
这是没有加tag的一行
    这是加了tag的一行
* 圆点测试
