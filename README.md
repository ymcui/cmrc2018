[**中文说明**](./README_CN.md) | [**English**](./README.md)

<p align="center">
    <br>
    <img src="./banner.png" width="500"/>
    <br>
</p>
<p align="center">
    <a href="https://github.com/ymcui/cmrc2018/blob/master/LICENSE">
        <img alt="GitHub" src="https://img.shields.io/github/license/ymcui/cmrc2018.svg?color=blue&style=flat-square">
    </a>
</p>

This repository contains the data for [The Second Evaluation Workshop on Chinese Machine Reading Comprehension (CMRC 2018)](https://hfl-rc.github.io/cmrc2018/). We will present our paper on [EMNLP 2019](http://emnlp-ijcnlp2019.org).

**Title: A Span-Extraction Dataset for Chinese Machine Reading Comprehension**    
Authors: Yiming Cui, Ting Liu, Wanxiang Che, Li Xiao, Zhipeng Chen, Wentao Ma, Shijin Wang, Guoping Hu   
Link: [https://www.aclweb.org/anthology/D19-1600/](https://www.aclweb.org/anthology/D19-1600/)  
Venue: EMNLP-IJCNLP 2019

### Open Challenge Leaderboard (New!)
Keep track of the latest state-of-the-art systems on CMRC 2018 dataset.  
[https://ymcui.github.io/cmrc2018/](https://ymcui.github.io/cmrc2018/)

### CMRC 2018 Public Datasets
Please download CMRC 2018 public datasets via the following CodaLab Worksheet.  
[https://worksheets.codalab.org/worksheets/0x92a80d2fab4b4f79a2b4064f7ddca9ce](https://worksheets.codalab.org/worksheets/0x92a80d2fab4b4f79a2b4064f7ddca9ce)

### Submission Guidelines
If you would like to **test your model on the hidden test and challenge set**, please follow the instructions on how to submit your model via CodaLab worksheet.  
[https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647/](https://worksheets.codalab.org/worksheets/0x96f61ee5e9914aee8b54bd11e66ec647/)

**Note that the test set on [CLUE](https://github.com/CLUEbenchmark/CLUE) is NOT the complete test set. If you wish to evaluate your model OFFICIALLY on CMRC 2018, you should follow the guidelines here.  **

### Quick Load Through 🤗datasets
You can also access this dataset as part of the [HuggingFace `datasets` library](https://github.com/huggingface/datasets) library as follow:

```python
!pip install datasets
from datasets import load_dataset
dataset = load_dataset('cmrc2018')
```
More details on the options and usage for this library can be found on the `nlp` repository at https://github.com/huggingface/nlp

### Reference
If you wish to use our data in your research, please cite:

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

### Official HFL WeChat Account
Follow Joint Laboratory of HIT and iFLYTEK Research (HFL) on WeChat.

![qrcode.png](./qrcode.jpg)

### Contact us
Please submit an issue.
