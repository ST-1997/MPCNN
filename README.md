# MPCNN论文复现	

##环境要求：
Python 3.6
Tensorflow 1.12.0
codes、nltk、numpy、embedding

##论文链接：
Multi-Perspective Sentence Similarity Modeling with Convolutional Neural Network paper 
link:http://www.emnlp2015.org/proceedings/EMNLP/pdf/EMNLP181.pdf

##参照的论文分析：
http://blog.csdn.net/liuchonge/article/details/62424805 http://blog.csdn.net/liuchonge/article/details/64128870 http://blog.csdn.net/liuchonge/article/details/64440110

##注意：
1.因为glove文件太大了没法上传，所以这里给出glove file的下载地址:http://nlp.stanford.edu/data/glove.6B.zip；
2.在glove.6B.300d.txt文件开始处加上400000 50，然后就可以用word2vec来读glove文件了。

##引用代码：
https://github.com/Fengfeng1024/MPCNN

##代码模块简单解释：
###data_helper.py数据集读取
主要完成数据的读取
###embedding.py词向量读入
主要完成词向量的读取
###model.py模型初始化
主要构建了一个MPCNN_Layer类来实现该论文的模型
###train.py模型训练
主要完成词向量、训练、测试数据的读取，模型的定义和训练，Summary的记录等工作
###utils.py余弦相似度计算
主要是几个函数：compute_l1_distance(x, y)、compute_euclidean_distance(x, y)、compute_cosine_distance(x, y)、comU1、comU2