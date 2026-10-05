# Dict查找
## 第 1 题：Two Sum

给你一个整数数组：

``nums = [2, 7, 11, 15]
target = 9`` 

请你写一个函数，返回两个数的下标，使它们的和等于 target。

要求：

``def two_sum(nums, target):
    ...``

输出：[0,1]


 def two_sum(nums,target):

    seen = {}
    
    for x,i in enumerate(nums):
    
        need = target - x
        
        if need in seen:
        
        return [seen[need],i]
        
        seen[x]=i 
        
        
这个就是用dict字典的存储key和value的特性，实现找搭档

## 题目 2：找重复元素

给你一个整数数组：

``nums = [4, 1, 7, 3, 1] ``

请写一个函数，返回第一个重复出现的数字。

 def first_appear(nums):

     seen = set()
     
     for x in nums:
     
         if x in seen:
         
            return x
            
         seen.add(x) 


## 题目3：找出现次数最多

nums = [2, 3, 2, 5, 3, 2, 4]

请写一个函数，返回出现次数最多的数字。

