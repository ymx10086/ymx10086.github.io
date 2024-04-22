---
title: "Python Big Data and Artificial Intelligence practice"
collection: courses_and_projects
type: "Undergraduate course"
permalink: /teaching/HUST-2023-PYTHON
venue: "Huazhong University of Science and Technology"
date: 2023-04-01
location: "Wuhan, Hubei"
---

This paper uses the third-party platform Rotten Tomatoes movie review dataset as the research object. Text sentiment analysis mainly includes the steps of data acquisition, preprocessing, classifier selection, emotion category output and so on. The difference between film review mining and other written review materials is that it includes not only the individual's views and opinions on the plot of the film, but also the subjective evaluation of the director, screenwriter, protagonist and other relevant characters of the film. The diversity of evaluation elements, the richness of emotional information and the flexibility of language expression make it difficult to analyze the emotional classification of film evaluation, but in-depth research has great theoretical and practical value.

以下为部分内容，其余请参见[仓库链接](https://github.com/ymx10086/HUST-2023-PYTHON)

本项目是针对于Kaggle中的烂番茄情感评论所设计的深度学习模型与框架，同时运用各种模型增强的方式和手段对于模型效果进行更好地提升。该文件是为了您更好地运行本项目，具体运行方法请见下。

下载库文件
=====

下载本项目用到的python库，如有不全，请自行下载。

pip install -r requirements.txt

获取数据
=====

本部分是为了获取GloVe: Global Vectors for Word Representation (stanford.edu)中的 pre-trained word vectors，通过加载glove为文本向量化做准备。

python fetch_data.py

数据准备
=====

本部分是为了处理数据，为了以后的训练模型和测试模型做准备。

cd sentiment-analysis-on-movie-reviews/scripts

python preprocessing.py

训练模型
=====

为了更加方便的进行训练模型的步骤，加载好的数据集已经放入data中，可以不进行之前步骤，直接进行模型的训练。

本部分是进行模型的训练，模型训练的参数如下：

checkpoint：加载预训练模型的相对路径

pretrain：预训练模型是否为MLM任务后得到的预训练模型

model：选择加载的模型

use_pgd：是否进行对抗训练

cd training

基于CNN的文本分类模型TextCNN
===

python train.py --model testcnn

基于RNN的BiLSTM模型
===

python train.py --model bilstm

BiGRU和注意力机制结合的深度模型
===

python train.py --model normal

基于Bert的大规模预训练模型Sibert
===

python process_SiBert.py

进行进一步预训练（MLM任务）
===

python pretrain.py

测试模型
=====

本部分是对于模型进行进一步的测试以获得submission.csv。

cd ../testing

基于CNN的文本分类模型TextCNN
===

python test.py --model testcnn

基于RNN的BiLSTM模型
===

python test.py --model bilstm

BiGRU和注意力机制结合的深度模型
===

python test.py --model normal

说明
=====

由于文件大小的限制，没有保存训练好的模型，只保存了模型的具体结果，请见submission。