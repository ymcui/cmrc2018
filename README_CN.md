[**中文说明**](./README_CN.md) | [**English**](./README.md)

## A Span-Extraction Dataset for Chinese Machine Reading Comprehension (CMRC 2018)
本目录包含[第二届“讯飞杯”中文机器阅读理解评测（CMRC 2018）]所使用的数据。本数据集已被计算语言学顶级国际会议[EMNLP 2019](http://emnlp-ijcnlp2019.org)录用。

**Title: A Span-Extraction Dataset for Chinese Machine Reading Comprehension**    
Authors: Yiming Cui, Ting Liu, Wanxiang Che, Li Xiao, Zhipeng Chen, Wentao Ma, Shijin Wang, Guoping Hu   
Link: [https://www.aclweb.org/anthology/D19-1600/](https://www.aclweb.org/anthology/D19-1600/)  
Venue: EMNLP-IJCNLP 2019

#### CMRC 2018 公开数据集
请通过CodaLab Worksheet下载CMRC 2018公开数据集（训练集，开发集）。
[https://worksheets.codalab.org/worksheets/0x92a80d2fab4b4f79a2b4064f7ddca9ce](https://worksheets.codalab.org/worksheets/0x92a80d2fab4b4f79a2b4064f7ddca9ce)

#### 提交方法
如果你想要在**隐藏的测试集、挑战集上测试你的模型**，请通过以下步骤提交你的模型。
[https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647/](https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647/)

#### 开放式挑战排行榜
想了解在CMRC 2018数据上表现最好的模型吗？请查阅排行榜。
[https://hfl-rc.github.io/cmrc2018/open_challenge/](https://hfl-rc.github.io/cmrc2018/open_challenge/)

#### 通过🤗nlp快速加载
你可以通过[HuggingFace `nlp` library](https://github.com/huggingface/nlp)工具包快速加载数据集：

```python
!pip install nlp
from nlp import load_dataset
dataset = load_dataset('cmrc2018')
```
关于`nlp`工具包的更多选项和使用细节可以通过这里访问了解：https://github.com/huggingface/nlp

### 引用
如果你在你的工作中使用了我们的数据，请引用下列文献：

```
@inproceedings{cui-emnlp2019-cmrc2018,
    title = "A Span-Extraction Dataset for {C}hinese Machine Reading Comprehension",
    author = "Cui, Yiming  and
      Liu, Ting  and
      Che, Wanxiang  and
      Xiao, Li  and
      Chen, Zhipeng  and
      Ma, Wentao  and
      Wang, Shijin  and
      Hu, Guoping",
    booktitle = "Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)",
    month = nov,
    year = "2019",
    address = "Hong Kong, China",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/D19-1600",
    doi = "10.18653/v1/D19-1600",
    pages = "5886--5891",
}
```
### International Standard Language Resource Number (ISLRN)
ISLRN: 013-662-947-043-2

http://www.islrn.org/resources/resources_info/7952/

## 哈工大讯飞联合实验室官方微信公众号
欢迎关注哈工大讯飞联合实验室（HFL）微信公众号，了解最新的技术动态。

![qrcode.png](https://github.com/ymcui/cmrc2018/blob/master/qrcode.jpg)

## 联系我们
请提交Issue。
