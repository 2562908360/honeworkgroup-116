# honeworkgroup-116  
The group 116  
这是网络空间安全创新创业第116小组的作业仓库  
该作业为独自完成，参考教程在project文档里有说明  
> # Project1  
>> - # Project1实验说明    
>>   - ## 生日概述  
>>     - 生日攻击是一种密码学攻击方法，利用生日悖论来寻找两个不同的输入，它们产生相同的哈希值或者其他指纹值。该攻击方法可以用于破解哈希函数的强度或者构造冲突。  
>>   - ## 实现方式  
>>     - ### 步骤一:选择哈希算法和哈希值长度  
>>       - 首先，选择要攻击的哈希算法和相应的哈希值长度。通常，生日攻击的难度随着哈希值长度的增加而增加。  
>>     - ### 步骤二:生成随机字符串  
>>       - 实现一个函数来生成随机字符串，以用作攻击过程中的输入。随机字符串的长度应该足够长，以提高碰撞的概率。  
>>     - ### 步骤三:构造哈希前缀集合  
>>       - 创建一个空的哈希前缀集合，用于存储已经计算过的哈希前缀。  
>>      - ### 步骤四:进行生日攻击  
>>       - 1、生成一个随机字符串。  
>>       - 2、对随机字符串进行哈希计算，获取其哈希值。  
>>       - 3、提取哈希值的前缀（长度根据选定的哈希算法和长度确定）。  
>>       - 4、检查哈希前缀是否存在于哈希前缀集合中。  
>>       - 5、如果存在，说明找到了两个不同的字符串，它们的哈希前缀相同，发现了碰撞。  
>>       - 6、如果不存在，将哈希前缀添加到哈希前缀集合中，继续下一轮循环。  
>>     - ### 步骤五:处理碰撞结果  
>>       - 一旦发现碰撞，可以获取碰撞的字符串和对应的哈希值，用于进一步分析和验证攻击的成功性。    
>>   - ## 运行效果  
>>     - ![image](https://github.com/2562908360/honeworkgroup-116/assets/97723386/b0071d01-2143-493c-b789-4279eec195ac)
>>     - CPU：AMD Ryzen 9 5900HX with Radeon Graphics           3.30 GHz
> # Project5  
>> - # Project5实验说明
>>   - ## Merkle Tree
>>     - Merkle Tree，通常也被称作Hash Tree，顾名思义，就是存储hash值的一棵树。Merkle树的叶子是数据块(例如，文件或者文件的集合)的hash值。非叶节点是其对应子节点串联字符串的hash。
>>     - Merkle树看起来非常像二叉树，其叶子节点上的值通常为数据块的哈希值，而非叶子节点上的值，所以有时候Merkle tree也表示为Hash tree,如下图所示：
>>     - ![image](https://github.com/2562908360/honeworkgroup-116/assets/97723386/a475be82-eb59-4cec-825e-3c72366c0d20)
>>   - ## 实现方式
>>     - 默克尔树节点定义：定义了一个 MerkleTreeNode 类，其中包含了左子节点、右子节点、父节点以及节点的值（哈希值）等属性。这个类用于构建树的节点。
>>     - 默克尔树结构定义：定义了一个 MerkleTree 类，其中包含了叶子节点列表、根节点以及用于存储整个树中节点值的 mtlist 列表。MerkleTree 类有以下几个重要方法：
>>       - `sha256_leaf(value)`: 这个方法用于计算叶子节点的哈希值。它对节点的值进行了级联操作，并使用 SHA-256 哈希算法对级联后的字符串进行哈希计算。
>>       - `sha256_node(value)`: 这个方法用于计算中间节点的哈希值。同样，它对节点的值进行了级联操作，并使用 SHA-256 哈希算法对级联后的字符串进行哈希计算。
>>       - `create_MerkleTree()`: 这个方法用于构建默克尔树。它先创建叶子节点，并对每个叶子节点计算其哈希值。然后，从叶子节点开始，逐层构建中间节点，直到生成根节点。中间节点的哈希值是由其两个子节点的哈希值计算得到。
>>       - `Inorder(root)`: 这个方法用于中序遍历整个默克尔树，得到树中所有节点的值，并存储在 mtlist 列表中。
>>       - `proof(root, nodevalue)`: 这个方法用于验证给定的节点值是否存在于默克尔树中。它通过调用 Inorder 方法得到整个树的节点值列表，并检查给定的节点值是否在其中，从而判断节点是否在树中。
>>     - 主程序部分：在主程序中，首先生成 10**5 个随机整数作为叶子节点的值，并将其转换为对应的十六进制表示。然后，利用这些叶子节点值构建默克尔树，并输出树的根节点的值。接着，验证一些随机生成的节点值是否在默克尔树中，并输出验证结果。




