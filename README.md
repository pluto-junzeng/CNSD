# CNSD

中文自然语言推理数据集（A large-scale Chinese Nature language inference and Semantic similarity calculation Dataset）
本数据及通过翻译加部分人工修正的方法，从英文原数据集生成，可以一定程度中文自然语言推理和语义相似度计算数据集不够的问题。

#### News

- 2020.01.13 正式中文版Squad-zen现已更新[访问链接](https://github.com/zengjunjun/ChineseSquad)

- 2019.12.01本数据集CMNLI 已被[CLUE](https://github.com/CLUEbenchmark/CLUE) 收录，详情请参考 CLUE 语言推理任务 Chinese Multi-Genre NLI。训练集与本数据集保持一致，dev和test有所改变

#### 论文地址(PrePrint)
arxiv 没有人邀请，只有野路子open了给大家参考下下0.0

[A large-scale Chinese Nature language inference and Semantic similarity calculation Dataset](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/CNSD.pdf?sign=401485f4d6f256393a264e68464ca4ae&t=1578114336)

#### 下载链接


- ALL-List : [腾讯云](http://ccnunlp.top/archives/filepath)
- Chinese-SNLI：[百度云链接](https://pan.baidu.com/s/1mt3Gl725bzACfsXUe9aNLw ) 提取码：cjob  [腾讯云](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/cnsd-snli.rar?sign=27370d06c74c6724e1f6c97f6ba1598a&t=1578114485)
- Chinese-MNLI: [百度云链接](https://pan.baidu.com/s/10yfCQw_mNQh4pB9ygBY8bg ) 提取码：txti [腾讯云](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/cnsd-mnli.rar?sign=6a432c19f657ad37e2ba504ddec0529f&t=1578114431)
- Chinese-QQP：[Quora Question Pairs](https://www.kaggle.com/c/quora-question-pairs/overview) 版权不明，暂不提供下载
- Chinese-STS-B : [腾讯云](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/STS-B.rar?sign=fa8d3ee7bc4e07d9ef64042f2d4f2465&t=1578114501)

#### 数据规模

|               | Train | Dev   | Test                 | Sum  |
| ------------- | ----- | ----- | -------------------- | ---- |
| Chinese-SNLI  | 550k  | 10k   | 10k                  | 570k |
| Chinese-MNLI  | 390k  | 12k   | 13k                  | 415k |
| Chinese-QQP   | 390k  | 8k    | 800k (without label) | 1.1m |
| Chinese-STS-B | 5.7k  | 1.5k  | 1.3k                 | 8.5k |
| Total         | 1.3m  | 31.5k | 824.3k               | 2.1m |

#### 数据格式
-  Chinese-SNLI & Chinese-MNLI
{
  "sentence1": "你敢不敢像拉斯柯尔尼科夫那样，勇于面对现实，拒绝那些管理小人物的琐碎规则？",
  "sentence2": "你会站起来揭发镇上所有的邪恶领主吗？",
  "gold_label": "neutral"
}
#### 实验结果



| Model                 | Chinese-SNLI | Chinese-SNLI | Chinese-MNLI | Chinese-MNLI | Chinese-QQP | Chinese-STS-B | Chinese-STS-B |
| --------------------- | ------------ | ------------ | ----------- | ----------- | ----------- | ----------- | ------------- |
|                       | Dev          | Test         | Mismatched  | Matched     | Dev         | Dev         | Test          |
| Embed+add-attention   | 74.46        | 75.05        | 63.28       | 62.25       | 72.56       | -           | -             |
| BiLSTM+self-attention | 81.19        | 80.96        | 69.47       | 67.79       | 81.45       | 43.87       | 41.24         |
| DiSAN                 | 81.32        | 81.45        | 69.54       | 68.13       | 82.32       | 44.21       | 42.09         |
| BERT                  | **87.39**    | **86.95**    | **79.76**   | **79.39**   | **89.08\*** | **53.84**   | **50.26**     |


####  参考


[A large annotated corpus for learning natural language inference](http://nlp.stanford.edu/pubs/snli_paper.pdf)

[A Broad-Coverage Challenge Corpus for Sentence Understanding through Inference](https://www.nyu.edu/projects/bowman/multinli/paper.pdf)

#### 致谢 
感谢腾讯云提供翻译服务

# 声明

本数据集只能用于学术研究，请勿用作商业
