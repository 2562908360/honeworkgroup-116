# honeworkgroup-116  
The group 116  
这是网络空间安全创新创业第116小组的作业仓库  
该作业为独自完成，参考教程在project文档里有说明 
1. Project1
# Project1实验说明    
## 生日概述  
生日攻击是一种密码学攻击方法，利用生日悖论来寻找两个不同的输入，它们产生相同的哈希值或者其他指纹值。该攻击方法可以用于破解哈希函数的强度或者构造冲突。  
## 实现步骤  
### 步骤一:选择哈希算法和哈希值长度  
首先，选择要攻击的哈希算法和相应的哈希值长度。通常，生日攻击的难度随着哈希值长度的增加而增加。  
### 步骤二:生成随机字符串  
实现一个函数来生成随机字符串，以用作攻击过程中的输入。随机字符串的长度应该足够长，以提高碰撞的概率。  
### 步骤三:构造哈希前缀集合  
创建一个空的哈希前缀集合，用于存储已经计算过的哈希前缀。  
### 步骤四:进行生日攻击  
1、生成一个随机字符串。  
2、对随机字符串进行哈希计算，获取其哈希值。  
3、提取哈希值的前缀（长度根据选定的哈希算法和长度确定）。  
4、检查哈希前缀是否存在于哈希前缀集合中。  
5、如果存在，说明找到了两个不同的字符串，它们的哈希前缀相同，发现了碰撞。  
6、如果不存在，将哈希前缀添加到哈希前缀集合中，继续下一轮循环。  
### 步骤五:处理碰撞结果  
一旦发现碰撞，可以获取碰撞的字符串和对应的哈希值，用于进一步分析和验证攻击的成功性。  
##执行结果  
![image](https://github.com/2562908360/honeworkgroup-116/assets/97723386/b0071d01-2143-493c-b789-4279eec195ac)



