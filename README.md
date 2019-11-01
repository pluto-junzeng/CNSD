# CNSD

中文自然语言推理数据集（A large-scale Chinese Nature language inference and Semantic similarity calculation Dataset）



#### 下载链接

百度网盘：链接：https://pan.baidu.com/s/1jqFVFLfmyaToeT3AM0UyqA   提取码：cu2m 





#### 数据规模

|               | Train | Dev   | Test                 | Sum  |      |
| ------------- | ----- | ----- | -------------------- | ---- | ---- |
| Chinese-SNLI  | 550k  | 10k   | 10k                  | 570k |      |
| Chinese-MNLI  | 390k  | 12k   | 13k                  | 415k |      |
| Chinese-QQP   | 390k  | 8k    | 800k (without label) | 1.1m |      |
| Chinese-STS-B | 5.7k  | 1.5k  | 1.3k                 | 8.5k |      |
| Total         | 1.3m  | 31.5k | 824.3k               | 2.1m |      |

#### 实验结果



| Model                 | Chinese-SNLI | Chinese-SNLI | Chinese-MNL | Chinese-MNL | Chinese-QQP | Chinese-QQP | Chinese-STS-B |
| --------------------- | ------------ | ------------ | ----------- | ----------- | ----------- | ----------- | ------------- |
| Dev                   | Test         | Mismatched   | Matched     | Dev         | Dev         | Test        |               |
| Embed+add-attention   | 74.46        | 75.05        | 63.28       | 62.25       | 72.56       | -           | -             |
| BiLSTM+self-attention | 81.19        | 80.96        | 69.47       | 67.79       | 81.45       | 43.87       | 41.24         |
| DiSAN                 | 81.32        | 81.45        | 69.54       | 68.13       | 82.32       | 44.21       | 42.09         |
| BERT                  | **87.39**    | **86.95**    | **79.76**   | **79.39**   | **89.08\*** | **53.84**   | **50.26**     |

#### 引用



# 声明

本数据集只能用于学术研究，请勿用作商业
