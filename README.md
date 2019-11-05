# Re-ID

Market 1501

Resnet50 :          batchsize=32 :         Rank1 =95.81    ,    mAP=88.28

+  RK (Re-Ranking):  Rank1 =96.25    ,     mAP=94.31



If you want a higher accuracy, you may  modify batchsize or use Resnet101.     
                 
                 
DukeMTMC-REID 

Resnet50:          batchsize =32 :        Rank1 =88.7      ,    mAP=77.9    

pytorch = 0.4


我已经把代码删除了，因为要用这个参加比赛，比赛完事后我会重新写上来，请见谅。



首先，采用human parsing对人体分割，结合金字塔水平分块策略，使得网络准确提取细粒度区域特征的能力大幅提升;

训练阶段，借鉴curriculum learning思路，难样本比例逐步提升，使得损失函数更易收敛;

通过图网络结构，学习得到各个细粒度特征的加权系数，进一步提高特征的分辨能力;

最后，在测试阶段，除常规距离计算手段，引入重构距离，提升网络对未对齐、遮挡等技术难点的健壮性。
