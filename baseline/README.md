# BERT Baselines for CMRC 2018 and DRCD
This repository contains the BERT baseline systems for CMRC 2018 and DRCD. 
These are two Chinese Span-Extraction Machine Reading Comprehension datasets (like SQuAD) publically available.

## Content

| Section | Description |
|-|-|
| [Datasets](#Datasets) | CMRC 2018 and DRCD |
| [Usage](#Usage) | How to train and test |
| [Baseline Results](#Baseline-Results) | BERT baseline results |

## Datasets
CMRC 2018 (Simplified Chinese): [https://github.com/ymcui/cmrc2018](https://github.com/ymcui/cmrc2018)

DRCD (Traditional Chinese): [https://github.com/DRCSolutionService/DRCD](https://github.com/DRCSolutionService/DRCD)

You can download these datasets through the links above, or alternatively, you can also download directly from `data` directory. Note that, we use SQuAD-like CMRC 2018 datasets, which could be accessed through [link](https://github.com/ymcui/cmrc2018/tree/master/squad-style-data).

For more Chinese machine reading comprehension datasets, please infer: [https://github.com/ymcui/Chinese-RC-Datasets](https://github.com/ymcui/Chinese-RC-Datasets)


## Dependency Requirements
There is nothing special dependency requirements, except for `TensorFlow==1.12`. Could also work on other versions of TensorFlow (not tested).

The code is based on official BERT implementation of `run_squad.py`.

Check: https://github.com/google-research/bert/blob/master/run_squad.py

## Usage
###  Step 1: Download BERT weights (skip if you have them)
- [Chinese (base)](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip)
- [Multi-lingual (base)](https://storage.googleapis.com/bert_models/2018_11_23/multi_cased_L-12_H-768_A-12.zip)

### Step 2: Set correct local variables
- `$PATH_TO_BERT`: the path to BERT weights (TensorFlow version)
- `$DATA_DIR`: the path to your dataset
- `$MODEL_DIR`: output directory for your model

### Step 3: Training
Then, we use the following script for training. We take CMRC 2018 dataset and multi-lingual BERT as an example.
```
python run_cmrc2018_drcd_baseline.py \
	--vocab_file=${PATH_TO_BERT}/multi_cased_L-12_H-768_A-12/vocab.txt \
	--bert_config_file=${PATH_TO_BERT}/multi_cased_L-12_H-768_A-12/bert_config.json \
	--init_checkpoint=${PATH_TO_BERT}/multi_cased_L-12_H-768_A-12/bert_model.ckpt \
	--do_train=True \
	--train_file=${DATA_DIR}/cmrc2018_train.json \
	--do_predict=True \
	--predict_file=${DATA_DIR}/cmrc2018_dev.json \
	--train_batch_size=32 \
	--num_train_epochs=2 \
	--max_seq_length=512 \
	--doc_stride=128 \
	--learning_rate=3e-5 \
	--save_checkpoints_steps=1000 \
	--output_dir=${MODEL_DIR} \
	--do_lower_case=False \
	--use_tpu=False
```

### Step 4: Evaluation
We use official evaluation script for CMRC 2018 and DRCD.
Note that, as DRCD official does not provide evaluation script, we also use `cmrc2018_evaluate.py` for DRCD.

`python cmrc2018_evaluate.py cmrc2018_dev.json predictions.json`


## Baseline Results
We provide both `BERT-Chinese` and `BERT-multilingual` baselines.

**Note that, each baseline is performed on 10 runs, and we take average scores of them for reliable results (do not applied on hidden sets).**

### CMRC 2018
| System  | DEV-EM | DEV-F1 | TEST-EM | TEST-F1 | CHALLENGE-EM | CHALLENGE-F1 | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| BERT (Multi-lingual) | 63.6 | 84.0 | 68.4 | 86.5 | 18.5 | 43.0 | - |
| BERT (Chinese) | 63.5 | 83.6 | 67.5 | 85.6 | 18.4 | 42.1 | - |
| P-Reader (single model) | 59.894 | 81.499 | 65.189 | 84.386 | 15.079 | 39.583 | - |
| GM-Reader (ensemble) | 58.931 | 80.069 | 64.045 | 83.046 | 15.675 | 37.315 | - |
| MCA-Reader (ensemble) | 66.698 | 85.538 | 71.175 | 88.090 | 15.476 | 37.104 | - | 
| Z-Reader (single model) | 79.776 | 92.696 | 74.178 | 88.145 | 13.889 | 37.422 | - |
| [SRC->DS(±) (Yang et al., 2019)](https://arxiv.org/abs/1904.06652) | 49.2 | 65.4 | - | - | - | - | - |

> Leaderboard: https://hfl-rc.github.io/cmrc2018/open_challenge/ </br>
> Note that, some of the previous submission are using development set for training as well.


### DRCD
| System  | DEV-EM | DEV-F1 | TEST-EM | TEST-EM | Note |
| :------ | :-----: | :-----: | :-----: | :-----: | :-----: |
| BERT (Multi-lingual) | 83.0 | 89.7 | 83.2 | 89.8 | - |
| BERT (Chinese) | 82.2 | 89.3 | 81.6 | 88.8 | - |
| [SRC + DS(±) (Yang et al., 2019)](https://arxiv.org/abs/1904.06652) | 55.4 | 67.7 | - | - | - |
| r-net (single model) | - | - | 29.1 | 44.4 | - |

## Contact
For help or issues, please submit a GitHub issue.
