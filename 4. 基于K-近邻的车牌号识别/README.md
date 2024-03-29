## 一、背景

图像的智能处理一直是人工智能领域广受关注的一类技术，代表性的如人脸识别与 CT 肿瘤识别，在人工智能落地的进程中发挥着重要作用。其中车牌号识别作为一个早期应用场景，已经融入日常生活中，为我们提供了诸多便利，在各地的停车场和出入口都能看到它的身影。车牌号识别往往分为字符划分和字符识别两个子任务，本案例我们将关注字符识别的任务，尝试用 K-NN 的方法对分割好的字符图像进行自动识别和转化。

## 二、任务

* 完成数据的读入和表示，将图片表示成向量并和 label 对应上；
* 分析当 K 取不同值时测试准确率的变化；
* 分析不同距离度量方式对模型效果的影响；
* 对比平权和加权 K-NN 的效果；
* 分析训练集大小对测试结果的影响。

## 三、评价指标
构建 K-NN 模型对测试集中的图片进行预测并计算准确率。

## 四、数据概览
按字符划分的车牌图片作为数据集，已放在在Data文件夹下，已经分成了训练集(train文件夹)和测试集（test文件夹）。训练集和测试集都分包括数字10个（0-9）、大写字母24个（A-Z，不包含 O 和 I）、省份简称31个，共计 65 个类（编号从 0 到 64）的20*20图片。文件夹名称即为标签。

## 五、模型训练过程、结果及详细对比
####  详见 train.ipynb

---
---
## 环境参考：

| model | version |
|----------|----------|
| python                    | 3.10.13 |
| matplotlib                | 3.4.3 |
| matplotlib-inline         | 0.1.6 |
| pandas                    | 1.5.3 |
| scikit-learn              | 1.3.0 |