---
title: BlockChain
date: 2019-07-23 16:47:05
categories: 区块链
tags:
  - 基础知识
---

# 区块链

## 学习链接

[Q 区块链-知乎](https://zhuanlan.zhihu.com/c_1005861027501768704)
再开始 EOSIO 的 training 前，建议小伙伴们可以看下，BTC 和 ETH 相关的白皮书
比特币白皮书: https://bitcoin.org/files/bitcoin-paper/bitcoin_zh_cn.pdf
比特币白皮书精读: https://www.jianshu.com/p/ca0c0a0e0faa 
白皮书官方地址：https://github.com/ethereum/wiki/wiki/White-Paper
社区中文版本：http://ethfans.org/wikis/以太坊白皮书
我也推荐两本：
《mastering bitcoin》: https://github.com/bitcoinbook/bitcoinbook 
《mastering ethereum》: https://github.com/ethereumbook/ethereumbook

## 学习摘要

### 白皮书精读 -- 大鱼
1. 原文中“我们定义，一枚电子货币（an electronic coin）是这样的一串数字签名”，很容易让人误解的是这里的电子货币是个具体数字，其实它是一条加密的记录（数据），也就是说你拥有的交易记录才是你的数字资产，这里面你需要注意的是，这条记录里面没有你的姓名、身份证号等这些中心化系统中常见的识别所有者的字段，唯一表示你身份的是你的公钥（钱包），证明你所有权的是你的私钥（密码）
2. 

### [必看:区块链概念与智能合约](https://zhuanlan.zhihu.com/p/40649384)

1. 区块链概念  
   ① 区块链如何存储与校验数据？  
   利用块链式数据结构来验证与存储数据 
   ② 区块链既然是分布式的数据库，那么这些分布的数据库按照什么规则进行同步？数据按照什么规则产生？  
   利用分布式节点共识算法来生成和更新数据  
   ③ 区块链既然是分布式的数据库，那么如何保证数据在节点间的网络传输安全？数据不被篡改？  
   利用密码学的方式保证数据传输和访问的安全  
   ④ 数据如何产生与使用？  
   利用由自动化脚本代码组成的智能合约来编程和操作数据
2. 智能合约是分布式的程序脚本。
3. 智能合约需要一个一般等价物。
4. 智能合约的执行结果需要达成共识。
5. 智能合约不是万能的，不是所有的合约都能转化为智能合约。

### [初识区块链](https://zhuanlan.zhihu.com/p/41283923)

1. 数字货币为什么有价值

   ① 数字货币发行是公开，没有中心化的发币机构

   传统的发币机构，可以用一张纸(印钱)掠夺收割人民的劳动成果。

   数字货币发行是取决于所有使用数字货币的人的共识。

   ② 数字货币的匿名性

   数字货币的排他性应用范围:黑产(黑色产业链)。

   ③ 财帛动人心,引起关注。

### [区块链技术基础：分布式账本简介-IBM Developer

](https://www.ibm.com/developerworks/cn/cloud/library/cl-blockchain-basics-intro-bluemix-trs/index.html)

1. 区块链到底是什么？  
   现在您能否向其他人解释“区块链”？  
   如果感到犹豫不决，并非只您一个人如此！我们的区块链入门手册实际解决了这个问题。请阅读它，并向您的家人、邻居和同事流利地表达您新掌握的概念！  
   区块链是一种防篡改的、共享的数字化账本，用于记录公有或私有对等网络中的交易。账本分发给网络中的所有成员节点，在通过哈希密码算法链接的区块的顺序链中，永久记录网络中的对等节点之间发生的资产交易的历史记录。  
   所有经过确认和证明的交易都从链的开头一直链接到最新的区块，因此得名区块链。区块链可以充当单一事实来源，而且区块链网络中的成员只能查看与他们相关的交易。

# 《区块链技术核心概念与原理》 -- 熊丽兵 Tiny

## 密码朋克 （Cypherpunk）

# 《区块链技术与应用》---肖臻
## 比特币
### 数据结构

1. 包括哈希指针(Hash Pointer)、默克尔树(Merkle Tree)、轻节点的默克尔证明(Merkle Proof)等概念。该视频隶属于北京大学计算机系肖臻老师的区块链公开课《区块链技术与应用》，

### 共识协议

1. coinbase tx 铸币
2. 数字货币交易需要防止 double spending attack
3. 分布式共识 distributed consensus
4. distributed hash table
5. FLP impossibility result （异步系统只要有一个 faulty，就是达不成共识）
6. CAP（Consistency， Availability， Partition tolerance） Theorem
7. Consensus in BitCoin
8. 最长合法链

### 比特币实现

1. 包括去中心化的分布式账本， UTXO (Unspent Transaction Output)、出块奖励、交易费、比特币中用到的数据结构以及对比特币的分叉攻击

### 网络

1. application layer： bitcoin block chain
2. network layer： P2P Overlay Network
3. nodes: super node, master node, seed node,
4. 特点：simple, robust, but not efficient
5. 区块限制 1M
6. best effort

### 分叉
1. state fork 
2. protocol fork
   1. hard fork-长久分叉，必须所有节点都更新才不会出现长久分叉
      1. 旧节点未更新新特性，不认同协议导致,直接分成2个币种或者两个社区
      2. block size limit 1M->4M  tx 250byte 10min/block  about 7tx/secs
   2. soft fork-临时分叉，算力50%以上更新就不会出现长久分叉

### 匿名性
1. anonymity privacy 
2. 零知识证明 -- 一方（证明者）向另一方（验证者）证明一个陈述是正确的，而无需透露除该陈述是正确外的任何信息
   1. 数学基础：同态隐藏
   2. 盲签方法
   3. 零币和零钞

### 总结
1. 不要被学术界的学术和程序员的思维限制了头脑和思维
2. 货币金融学
3. 量子计算相关知识了解
4. sha-256哈希算法


## 深入浅出RAFT共识算法
### 解决问题：
1.  分布式一致性问题：server端有2个、3个甚至更多节点，要怎么达成一致性
### RAFT共识算法
1.  Paxos算法难理解，即便现在放到很多高校，依然很多学生、教授都反馈Paxos算法难以理解。同时，Paxos算法在实际应用实现的时候也是比较困难的
2.  Raft是实现分布式共识的一种算法，主要用来管理日志复制的一致性。它和Paxos的功能是一样，但是相比于Paxos，Raft算法更容易理解、也更容易应用到实际的系统当中。而Raft算法也是联盟链采用比较多的共识算法。
3.  区块链分为：公有链、联盟链和私有链
4.  Raft的三种状态：
    1.  Follower（群众）：被动接收Leader发送的请求。所有的节点刚开始的时候是处于Follower状态。
    2.  Candidate（候选人）：由Follower向Leader转换的中间状态
    3.  Leader（领导）：负责和客户端交互以及日志复制（日志复制是单向的，即Leader发送给Follower），同一时刻最多只有1个Leader存在。
5.  关键概念
    1.  复制状态机
    2.  任期（Term）概念
    3.  心跳（heartbeats）和超时机制（timeout）
6.  Raft算法可以分为如下3个部分
    1.  领导人选举（Leader Election）
    2.  日志复制（Log Replication）leader节点日志覆盖follower
    3.  安全性 
    4.  

## 以太坊
### 概述
1. 区块链1.0 BTC  区块链2.0 以太坊
2. 内存hard mining puzzle 减少asic芯片的使用
3. proof of work（工作量证明）  -》》》  proof of stake（权益证明）
4. 区块生成速度由10分钟到秒级
5. 对于智能合约的支持 smart contract
6. BTC基于交易的账户模型（隐私保护较好），没有基于账户的管理，每次转账需要把所有币都转出，剩下的放入新地址
7. eth账户模型（合约需要参与者拥有较为稳定的身份）
   1. replay attack
   2. 外部账户或者普通账户  balance+nonce
   3. 合约账户   balance+nonce+code+storage 不能发起交易
8. 比特币依照这个范式，检查一个区块是否有效的算法如下：
   1. 检查区块引用的上一个区块是否存在且有效。
   2. 检查区块的时间戳是否晚于以前的区块的时间戳，而且早于未来2小时[2]。
   3. 检查区块的工作量证明是否有效。
   4. 将上一个区块的最终状态赋于S[0]。假设TX是区块的交易列表，包含n笔交易。对于属于0……n-1的所有i,进行状态转换S[i+1] = APPLY(S[i],TX[i])。如果任何一笔交易i在状态转换中出错，退出程序，返回错误。返回正确，状态S[n]是这一区块的最终状态。
9. 比特币网络每隔2016个区块重新设定目标数值，保证平均每十分钟生成一个区块，大概14天
10. 比特币系统的脚本语言存在一些严重的限制:
    1.  缺少图灵完备性:尽管比特币脚本语言可以支持多种计算，但是它不能支持所有的计算。最主要的缺失是循环语句。
    2.  价值盲（Value-blindness）:UTXO脚本不能为账户的取款额度提供精细的的控制。
    3.  缺少状态:UTXO只能是已花费或者未花费状态，这就没有给需要任何其它内部状态的多阶段合约或者脚本留出生存空间。
    4.  区块链盲（Blockchain-blindness）:UTXO看不到区块链的数据
11. 状态是由被称为“账户”（每个账户由一个20字节的地址）的对象和在两个账户之间转移价值和信息的状态转换构成的。以太坊的账户包含四个部分：
    1.  随机数，用于确定每笔交易只能被处理一次的计数器
    2.  账户目前的以太币余额
    3.  账户的合约代码，如果有的话
    4.  账户的存储（默认为空）
12. DAG 技术即 Directed Acyclic Graph （DAG），也叫有向无环图，是在分布式的分散环境中人们发送数据的另一种方法，不是区块链技术。它原本是计算机的一种数据结构，一般用来处理动态规划问题。最早提出这个概念的是 Sergio Demian Lerner，在 2015 年 9 月发表了《DAG Coin Draft》的文章，最早提出了 DAG-chain （DAG 链）的概念。
13. 一般来讲，以太坊之上有三种应用。第一类是金融应用，为用户提供更强大的用他们的钱管理和参与合约的方法。包括子货币，金融衍生品，对冲合约，储蓄钱包，遗嘱，甚至一些种类的全面的雇佣合约。第二类是半金融应用，这里有钱的存在但也有很重的非金钱的方面，一个完美的例子是为解决计算问题而设的自我强制悬赏。最后，还有在线投票和去中心化治理这样的完全的非金融应用。
14. 


# 《EOS Training》
## SmartContract 101
1. 所有都是基于account，account来做各种操作
2. EOSIO的智能合约运行在WASM（WebAssembly）
3. ABI Application Binary Interface
4. Interact With state 通过状态相互联系，状态机制？
5. 所有EOSIO操作需要资源，Resource，RAM，CPU，NET
6. E代表熵。 R是可用字符数。 L是密码的长度。您还可以通过首先计算可用字符数（R）到密码（L）中字符数的幂，然后计算结果的二进制对数（log 2 ）来获得密码的熵（E） = log 2 （R^L ））。


