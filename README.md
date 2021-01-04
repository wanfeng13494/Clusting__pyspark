# 部署操作
## 1.此项目为pyspark版本（原生版本请戳 👉 https://github.com/wanfeng13494/Clusting__SKlearn）
   ### 部署前需要先配置pyspark环境
   ### 具体请参考 👉 https://zhuanlan.zhihu.com/p/129061994
## 2.下载Gaia-DR3数据（此处附带一份我自己用的数据）
## 3.将代码中涉及到数据地址的语句改成自己的本地数据地址
## 4.补充下载代码中所需要的第三方库（部分库未用到，可删除）
## 5.运行（确保pyspark正常启动）

# 基于 DBSCAN 聚类算法在 Gaia-DR3 中疏散星团的成员判定
## 本项目基于GaiaDataRelease3 (Gaia DR3)星表,
## 采用数据挖掘技术中的DBSCAN(Density-Based Spatial Clustering of Applications with Noise)算法进行疏散星团成员判定.
## 从Gaia DR3中选取了113086颗恒星作为样本,
## 使用恒星的五维数据 (三维空间位置和两维自行)进行聚类分析.
## 在数据预处理阶段,将每一维数据标准化到[0,1]区间内,避免了单位不一致对聚类效果的影响.
## 然后,利用KD树搜索算法绘制k-dist图确定了DBSCAN算法的输入参数(Eps,MinPts).
## 最终,使用DBSCAN算法获取了一些成员星,分析结果表明得到的成员星是可靠的.
