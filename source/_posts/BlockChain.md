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
[比特币白皮书](https://bitcoin.org/files/bitcoin-paper/bitcoin_zh_cn.pdf)
[比特币白皮书精读](https://www.jianshu.com/p/ca0c0a0e0faa)
[白皮书官方地址](https://github.com/ethereum/wiki/wiki/White-Paper)
[以太坊白皮书-社区中文版本](http://ethfans.org/wikis/以太坊白皮书)
[mastering bitcoin](https://github.com/bitcoinbook/bitcoinbook) 
[mastering ethereum](https://github.com/ethereumbook/ethereumbook)
[区块链技术指南-yeasy](https://yeasy.gitbook.io/blockchain_guide)

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


# 《区块链技术指南-yeasy》
## 分布式系统核心技术
### 一致性问题
1. 一致性问题是分布式领域最基础、最重要的问题
2. 定义 一致性（Consistency），早期也叫（Agreement），在分布式系统领域中是指对于多个服务节点，给定一系列操作，在约定协议的保障下，使得它们对处理结果达成“某种程度”的协同。
3. 一致性关注的是系统呈现的状态，并不关注结果是否正确；例如，所有节点都对某请求达成否定状态也是一种一致性。
4. 将可能引发不一致的并行操作进行串行化。这实际上也是现代分布式系统处理一致性问题的基础思路
5. 规范来看，分布式系统达成一致的过程，应该满足：
    可终止性（Termination）：一致的结果在有限时间内能完成；
    约同性（Agreement）：不同节点最终完成决策的结果是相同的；
    合法性（Validity）：决策的结果必须是某个节点提出的提案。
6. 解决分布式系统领域很多问题的核心秘诀：把不同时空发生的多个事件进行全局唯一排序，而且这个顺序还得是大家都认可的。
7. 强一致性主要包括顺序一致性（Sequential Consistency）和线性一致性（Linearizability Consistency：
   1. 顺序一致性：又叫因果一致性，所有进程看到的全局执行顺序（total order）一致（否则数据副本就不一致了）；并且每个进程看自身操作的顺序（local order）跟实际发生顺序一致。
   2. 线性一致性：由 Maurice P. Herlihy 与 Jeannette M. Wing 在 1990 年经典论文《Linearizability: A Correctness Condition for Concurrent Objects》中共同提出，是最强的一致性。它在顺序一致性前提下增加了进程间的操作顺序要求，形成理想化完全一致的全局顺序。
8. 放宽对一致性的要求，采用部分异步操作，从而提升性能、可扩展性，降低响应延迟，这些在某些方面弱化的一致性都笼统称为弱一致性

### 共识算法
1. 而共识，则特指在分布式系统中多个节点之间对某个事情（例如多个事务请求，先执行谁？）达成一致看法的过程。因此，达成某种共识并不意味着就保障了一致性。
2. 根据解决的场景是否允许拜占庭错误情况，共识算法可以分为 Crash Fault Tolerance (CFT) 和 Byzantine Fault Tolerance（BFT）两类。对于非拜占庭错误的情况，已经存在不少经典的算法，包括 Paxos（1990 年）、Raft（2014 年）及其变种等。这类容错算法往往性能比较好，处理较快，容忍不超过一半的故障节点。对于要能容忍拜占庭错误的情况，包括 PBFT（Practical Byzantine Fault Tolerance，1999 年）为代表的确定性系列算法、PoW（1997 年）为代表的概率算法等。确定性算法一旦达成共识就不可逆转，即共识是最终结果；而概率类算法的共识结果则是临时的，随着时间推移或某种强化，共识结果被推翻的概率越来越小，最终成为事实上结果。拜占庭类容错算法往往性能较差，容忍不超过 1/3 的故障节点
3. 即便在网络通信可靠情况下，一个可扩展的分布式系统的共识问题通用解法的下限是——没有下限（无解）。

### FLP 不可能原理
1. 在分布式系统中，同步和异步这两个术语存在特殊的含义：
   1. 同步，是指系统中的各个节点的时钟误差存在上限；并且消息传递必须在一定时间内完成，否则认为失败；同时各个节点完成处理消息的时间是一定的。因此同步系统可以轻易判断是节点宕机还是传输消息丢失；
   2. 异步，则意味着系统中各个节点可能存在较大的时钟差异；同时消息传输时间是任意长的；各节点对消息进行处理的时间也可能是任意长的。这就造成无法判断某个消息迟迟没有被响应是哪里出了问题（节点故障还是传输故障？）。不幸地是，现实生活中的系统往往都是异步系统。

### CAP原理
1. 分布式系统无法同时确保一致性（Consistency）、可用性（Availability）和分区容忍性（Partition），设计中往往需要弱化对某个特性的需求。
2. 一致性、可用性和分区容忍性的具体含义如下：
   1. 一致性（Consistency）：任何事务应该都是原子的，所有副本上的状态都是事务成功提交后的结果，并保持强一致；
   2. 可用性（Availability）：系统（非失败节点）能在有限时间内完成对操作请求的应答；
   3. 分区容忍性（Partition）：系统中的网络可能发生分区故障（成为多个子网，甚至出现节点上线和下线），即节点之间的通信无法保障。而网络故障不应该影响到系统正常服务。
3. CAP 原理认为，分布式系统最多只能保证三项特性中的两项特性。
4. 网络分区是可能存在的，出现分区情况后很可能会导致发生“脑裂”现象。

### ACID 原则与多阶段提交
1. ACID，即 Atomicity（原子性）、Consistency（一致性）、Isolation（隔离性）、Durability（持久性）四种特性的缩写。
2. ACID 原则描述了分布式数据库需要满足的一致性需求，同时允许付出可用性的代价。
   1. Atomicity：每次事务是原子的，事务包含的所有操作要么全部成功，要么全部不执行。一旦有操作失败，则需要回退状态到执行事务之前；
   2. Consistency：数据库的状态在事务执行前后的状态是一致的和完整的，无中间状态。即只能处于成功事务提交后的状态；
   3. Isolation：各种事务可以并发执行，但彼此之间互相不影响。按照标准 SQL 规范，从弱到强可以分为未授权读取、授权读取、可重复读取和串行化四种隔离等级；
   4. Durability：状态的改变是持久的，不会失效。一旦某个事务提交，则它造成的状态变更就是永久性的。
3. 与 ACID 相对的一个原则是BASE（Basic Availability，Soft-state，Eventual Consistency）原则面向大型高可用分布式系统，主张牺牲掉对强一致性的追求，而实现最终一致性，来换取一定的可用性。
4. ACID 和 BASE 在英文中分别是“酸”和“碱”，看似对立，实则是对 CAP 三特性的不同取舍。
5. 两阶段提交算法：在分布式场景下，直接提交事务可能出现各种故障和冲突，那么可将其分解为预提交和正式提交两个阶段，规避风险
   1. 预提交（PreCommit）：协调者（Coordinator）发起执行某个事务的执行并等待结果。各参与者（Participant）执行事务但不提交，反馈是否能完成，并阻塞等待协调者指令；
   2. 正式提交（DoCommit）：协调者如果得到所有参与者的成功答复，则发出正式提交指令，否则发出状态回滚指令。
6. 三阶段提交算法针对两阶段提交算法第一阶段中参与者阻塞问题进行了优化。具体来说，将预提交阶段进一步拆成两个步骤：询问提交和预提交
   1. 询问提交（CanCommit）：协调者询问参与者是否能进行某个事务的提交。参与者需要返回答复是否准备好，但无需执行提交，也无需阻塞。这就避免出现参与者被阻塞的情况；
   2. 预提交（PreCommit）：协调者检查收集到的答复，如果全部为真，则发起执行事务请求。各参与参与者（Participant）需要执行事务但不提交，并反馈能否完成。注意此时说明所有参与者都已经处于准备好状态。；
   3. 正式提交（DoCommit）：协调者如果得到所有参与者的成功答复，则发出正式提交请求，否则发出状态回滚指令。本阶段时，如果参与者一直收不到请求，则超时后继续提交。
7. 三阶段提交主要解决了阻塞问题和协调者单点故障问题

### Paxos 算法与 Raft 算法
1. Paxos 问题是指分布式的系统中存在故障（crash fault），但不存在恶意（corrupt）节点的场景（即可能消息丢失或重复，但无错误消息）下如何达成共识

### 拜占庭容错

## 密码学与安全技术

### 密码学简史
1. 密码学可以大致分为古典密码学和近现代密码学两个阶段。两者以现代信息技术的诞生为分界点，现在所讨论的密码学多是指后者，建立在信息论和数学成果基础之上。
2. 

### hash算法与数字摘要
1. 一个优秀的 Hash 算法，将能满足：
   1. 正向快速：给定原文和 Hash 算法，在有限时间和有限资源内能计算得到 Hash 值；
   2. 逆向困难：给定（若干）Hash 值，在有限时间内无法（基本不可能）逆推出原文；
   3. 输入敏感：原始输入信息发生任何改变，新产生的 Hash 值都应该发生很大变化；
   4. 碰撞避免：很难找到两段内容不同的明文，使得它们的 Hash 值一致（即发生碰撞）。
2. 盐（Salt）是在获取密码hash后，通过盐再次加密，将盐和hash结果存放不同地方，只要不是两者同时泄漏，攻击者就很难破解

### 加解密算法
1. 加解密算法是现代密码学核心技术，从设计理念和应用场景上可以分为两大基本类型：对称加密、非对称加密
   1. 对称加密
      1. 优点是加解密效率（速度快，空间占用小）和加密强度都很高
      2. 缺点是参与方需要提前持有密钥，一旦有人泄露则系统安全性被破坏；另外如何在不安全通道中提前分发密钥也是个问题，需要借助额外的 Diffie–Hellman 协商协议或非对称加密算法来实现
   2. 非对称加密
      1. 