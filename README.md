# Chinese Instruction Datasets for LLMs

人人都爱ChatGPT，但是只有少数大型科技企业或实验室才有实力训练出这样的模型。最近，开源社区流行一种[Self-Instruct](https://arxiv.org/abs/2212.10560)做法：通过ChatGPT创建指令数据集(Instruction datasets)，然后在小规模LLM (比如[LLaMA 7B](https://github.com/facebookresearch/llama))上进行fine-tuning，也能得到"媲美"ChatGPT的效果。其中一个典型工作是[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)。

目前开源的指令数据集非常少并且主要是英文，仅有的几个中文指令数据集也是在英文数据集上进行翻译得到的，但考虑到大家对ChatGPT的强烈需求，我们相信后续会有越来越多的大规模中文指令数据集出现。

本项目旨在收集中文指令数据集，以便于大家能够更方便地对中文LLM进行fine-tuning。

|Dataset|Size|Description|Source|
|:----:|:----:|:----:|:----:|
|[Guanaco Dataset](https://huggingface.co/datasets/JosephusCheung/GuanacoDataset) | 27808|多语言指令数据集，规模还会更新至92530| [Guanaco](https://guanaco-model.github.io/) |
|[alpaca_chinese_dataset](https://github.com/hikariming/alpaca_chinese_dataset)|更新中|将Alpaca数据集进行机器翻译+人工校验，并补充一些对话数据|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)
|[alpaca-chinese-dataset](https://github.com/carbonz0/alpaca-chinese-dataset)|20465|将Alpaca数据集进行机器翻译得到|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)|
|[Chinese-alpaca-lora](https://github.com/LC1332/Chinese-alpaca-lora)|更新中|将Alpaca数据集进行机器翻译得到，翻译模型是gpt-3.5-turbo, 后续会结合Guanaco数据集|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)|
