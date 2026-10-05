# Dict查找 / 哈希查找 Dict这个集的底层逻辑就是哈希表实现的
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
思路提示：1.dict中的key存什么？2.value存什么? 这一题就是提示我们key value未必一定是数和下标这种关系，对应的映射都可以存的
{数值；出现的次数}

def most_frequent(nums):
    seen = {}
    for x in nums:
        if x in seen:
        seen[x] = seen[x] + 1
    if x != null:
       seen[x] = seen[x]
    seen[x] = 0
    return[max(seen)]    
这个代码有很多问题，不过思路是对的，就是检查一下如果出现了就给他次数+1，只不过如果没出现过的应该直接给x的value记为1即可了，最后return[max(seen)]   ，这个默认是根据key的大小来排，可以如下改进

def most_frequent(nums):
    seen={}
    for x in nums:
        if x in seen:
           seen[x] = seen[x] + 1
        else:
           seen[x] = 1
    return[max(seen,key=seen.get)] 这样就可以根据key对于的value来比较大小
    
## 题目 4：找第一个只出现一次的字符
给你字符串：

s = "swiss"

请返回第一个只出现一次的字符。

答案应该是：

"w"

def first_unique_char(s):
    count = {}
    for ch in s:
        if ch in count:
           count[ch] =+ 1
        else:
            count[ch] = 1
    for ch in s:
        if count[ch] ==1：
           return ch
           
        
            
        

