# mnist_clf
手写数字识别

0到9的手写数字图片 每张图片大小均为28*28*1（黑白图片）
训练集55000
测试集5000

网络结构为
X输入 28*28 reshape为 【1，28,28,1】的结构 分别表示 每批数 高 宽 通道数

第一层卷积层 kernel 3*3 总数32个

第二层卷积层 kernel 3*3 总数64个

第三次为池化层 采用最大池化 2*2 

然后将池化层的输出平摊

第四层为全连接层 激活函数relu

第五层全连接层 激活函数softmax输出每一类的概率

训练采用随机梯度下降 epoch100次
