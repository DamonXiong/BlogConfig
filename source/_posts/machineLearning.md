---
title: machineLearning
date: 2019-04-28 09:54:07
categories:
tags: 
    - 机器学习
---

# 《深度学习入门-基于Python的理论与实现》
## 学习摘要
1. 有兴趣可以读《计算机系统要素：从零开始构建现代计算机》
2. 感知机是具有输入和输出的算法。
3. 感知机将权重和偏置设定为参数
4. 单层感知机只能表示线性空间，而多层感知机可以表示非线性空间
5. 多层感知机可以表示计算机


# 《Python+Tensorflow机器学习实战》
## 环境搭建

```  
wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-5.3.0-Linux-x86_64.sh  
chmod -R a+x Anaconda3-5.3.0-Linux-x86_64.sh  
bash Anaconda3-5.3.0-Linux-x86_64.sh  
conda create -n tf-cpu tensorflow  
conda activate tf-cpu
conda deactivate tf-cpu  
```  

# 《Python机器学习及实践---- 从零开始通往Kaggle竞赛之路》 -- 范淼、李超
## 简介
1. 监督学习和无监督学习
   > 监督学习关注对事物未知表现的预测，一般包括分类问题(Classification、对所在的类别进行预测)和回归问题(Regression、对连续变量进行预测)  

   > 无监督学习倾向于对事物本身特性的分析，常用的技术包括数据降维(Dimensionality Reduction、对事物的特性进行压缩和筛选)和聚类问题(Clustering、依赖数据的相似性，把相似的数据样本划分为一个簇)等
2. 性能：评价所完成任务质量的指标。

## 基础
### 监督学习经典模型
1. ![监督学习基本架构和流程](./machineLearning/监督学习基本架构和流程.png)



# 《机器学习算法基础》--覃秉丰
## 课程链接
[机器学习算法基础](https://edu.51cto.com/course/16585.html)

## 课程笔记
1. 知识框架
   ![知识框架](./machineLearning/机器学习知识框架.png)
2. Anaconda安装Python及部分库
3. ![训练集-验证集-测试集](./machineLearning/训练集-验证集-测试集.png)
4. 学习方式：
   1. 监督学习：用来训练带有标签的数据集
   2. 无监督学习：用来训练没有标签的数据集
   3. 半监督学习：监督学习和无监督学习结合的一种学习方式。主要是用来解决使用少量标签的数据和大量没有标签的数据进行训练和分类问题。
5. 常见应用
   1. 回归
   2. 分类
   3. 聚类
6. 一元线性回归
   1. ![训练集-验证集-测试集](./machineLearning/一元线性回归.png)
7. 代价函数（Cost Function）
   1. ![最小二乘法](./machineLearning/最小二乘法.png)
   2. ![相关系数](./machineLearning/相关系数.png)
   3. ![决定系数](./machineLearning/决定系数.png)
8. 梯度下降法（优化算法）
   1. ![梯度下降法](./machineLearning/梯度下降法.png)
   2. ![局部最小值问题](./machineLearning/局部最小值问题.png)
   3. ![梯度下降法求线性回归](./machineLearning/梯度下降法求线性回归.png)
   4. ![梯度下降法求线性回归2](./machineLearning/梯度下降法求线性回归2.png)
   5. 非凸函数使用梯度下降法可能只能获取局部最小值，线性回归是凸函数，可以使用梯度下降法
9. 多元线性回归
   1.  ![多元线性回归模型](./machineLearning/多元线性回归模型.png)
10. 多项式回归
    1.  y=c+bt+at^2(次方数可再次增加)
11. 标准方程法
    1.  ![标准方程法](./machineLearning/标准方程法.png)
    2.  ![标准方程法](./machineLearning/标准方程法2.png)
    3.  ![矩阵不可逆情况](./machineLearning/矩阵不可逆情况.png)
    4.  ![梯度下降对比标准方程](./machineLearning/梯度下降对比标准方程.png)
12. 特征缩放
    1.  ![数据归一化](./machineLearning/数据归一化.png)
    2.  ![均值标准化](./machineLearning/均值标准化.png)
13. 交叉验证法
    1.  ![交叉验证法](./machineLearning/交叉验证法.png)
14. 拟合
    1.  ![拟合](./machineLearning/拟合.png)
    2.  ![防止过拟合](./machineLearning/防止过拟合.png)
    3.  ![正则化](./machineLearning/正则化.png)
15. 岭回归
    1.  ![岭回归](./machineLearning/岭回归.png)
    2.  ![岭回归](./machineLearning/岭回归2.png)
16. LASSO
    1.  ![LASSO](./machineLearning/LASSO.png)
    2.  ![LASSO与岭回归](./machineLearning/LASSO与岭回归.png)
    3.  ![LASSO与岭回归2](./machineLearning/LASSO与岭回归2.png)
    4.  ![LASSO与岭回归3](./machineLearning/LASSO与岭回归3.png)
17. 弹性网-2005年提出
    1.  ![弹性网](./machineLearning/弹性网.png)
    2.  ![弹性网正则式](./machineLearning/弹性网2.png)
    3.  结合岭回归和LASSO



# 《Python3入门机器学习经典算法与应用》--慕课网
## 课程摘要
### 简介
1. ![弹性网正则式](./machineLearning/机器学习算法.png)
2. ![机器学习学习注意点](./machineLearning/机器学习学习注意点.png)
### 第2章 机器学习基础
1. 大写字母代表矩阵，小写代表向量
2. ![数据](./machineLearning/数据.png)
3. 特征向量一般表征为列向量。行向量转置为列向量
4. 图像，每一个像素点都是特征。特征可以抽象。
5. 二分类和多分类：结果一个类别。
6. 回归任务：结果是一个连续数字的值，而非一个类别
7. 一些情况下，回归任务可以简化成分类任务，问题转化。
8. 监督学习：主要解决分类和回归。
9. 机器学习算法上分类：监督学习，非监督学习，半监督学习和增强学习。
10. 监督学习
    1.  给机器的训练数据拥有“标记”或者“答案”
    2.  主要处理两大类：回归和分类
    3.  ![监督学习算法.png](.\machineLearning/监督学习算法.png)
11. 非监督学习
    1.  给机器的训练数据没有任何“标记”或者“答案”
    2.  对没有“标记”的数据进行分类-聚类分析
    3.  对数据进行降维处理：
        1.  特征提取
        2.  特征压缩：PCA
        3.  意义：方便可视化
    4.  异常检测
12. 半监督学习
    1.  一部分数据有“标记”或者“答案”，另一部分数据没有
    2.  常见：各种原因产生的标记缺失
    3.  通常使用无监督学习手段对数据做处理，之后使用监督学习手段做模型的训练和预测
13. 增强学习
    1.  ![增强学习](.\machineLearning/增强学习.png)
14. 批量学习和在线学习
    1.  ![批量学习](.\machineLearning/批量学习.png)
    2.  ![批量学习优缺点](.\machineLearning/批量学习优缺点.png)
    3.  ![在线学习](.\machineLearning/在线学习.png)
    4.  ![在线学习优缺点](.\machineLearning/在线学习优缺点.png)
15. 参数学习和非参数学习
    1.  ![参数学习特点](.\machineLearning/参数学习特点.png)
    2.  ![非参数学习](.\machineLearning/非参数学习.png)
16. “哲学”思考
    1.  ![数据即算法](.\machineLearning/数据即算法.png)
    2.  算法为王？
    3.  奥卡姆的剃刀---简单就是好的
    4.  没有免费的午餐定理---可以严格的数学推导出：任意两个算法，他们的期望性能是相同的！
    5.  具体到某个特定问题，有些算法可能更好。
    6.  没有一种算法，绝对比另一种算法好
    7.  脱离具体的问题，谈哪个算法好是没有意义的。
    8.  在面对一个具体问题的时候，尝试使用多重算法进行比对试验，是必要的
    9.  机器伦理学
17. Numpy使用
    1.  random、arange等接口