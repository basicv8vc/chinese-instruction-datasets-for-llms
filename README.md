# Chinese Instruction Datasets for LLMs

人人都爱ChatGPT，但是只有少数大型科技企业或实验室才有实力训练出这样的模型。最近，开源社区流行一种[Self-Instruct](https://arxiv.org/abs/2212.10560)做法：通过Instruct/ChatGPT创建指令数据集(Instruction datasets)，然后在小规模LLM (比如[LLaMA 7B](https://github.com/facebookresearch/llama))上进行fine-tuning，也能得到"媲美"ChatGPT的效果。其中一个典型工作是[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)。

目前开源的指令数据集非常少并且主要是英文，仅有的几个中文指令数据集也是在英文数据集上进行翻译得到的，但考虑到大家对ChatGPT的强烈需求，我们相信后续会有越来越多的大规模中文指令数据集出现。

本项目旨在收集中文指令数据集，以便于大家能够更方便地对中文LLMs进行fine-tuning。

|Dataset|Size|Description|Source|
|:----:|:----:|:----:|:----:|
|[Guanaco Dataset](https://huggingface.co/datasets/JosephusCheung/GuanacoDataset) | 27808|多语言指令数据集，规模还会更新至92530| [Guanaco](https://guanaco-model.github.io/) |
|[alpaca_chinese_dataset](https://github.com/hikariming/alpaca_chinese_dataset)|正在更新中|将Alpaca数据集进行机器翻译+人工校验，并补充一些对话数据|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)
|[alpaca-chinese-dataset](https://github.com/carbonz0/alpaca-chinese-dataset)|20465|将Alpaca数据集进行机器翻译得到|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)|
|[Chinese-alpaca-lora](https://github.com/LC1332/Chinese-alpaca-lora)|更新中|将Alpaca数据集进行机器翻译得到，翻译模型是gpt-3.5-turbo, 后续会结合Guanaco数据集|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)|
|[GPT-4-LLM](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM)|52k|将Alpaca数据集的prompt利用ChatGPT进行翻译，然后利用GPT-4得到中文Response|[Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca)|
|[BelleGroup/train_0.5M_CN](https://huggingface.co/datasets/BelleGroup/train_0.5M_CN)|0.5M|作者创建的[中文种子prompt](https://github.com/LianjiaTech/BELLE/blob/main/1.5M/zh_seed_tasks.json)，利用text-davinci-003得到Response|[BELLE](https://github.com/LianjiaTech/BELLE)|
|[BelleGroup/train_1M_CN](https://huggingface.co/datasets/BelleGroup/train_1M_CN)|1M|[中文种子prompt](https://github.com/LianjiaTech/BELLE/blob/main/1.5M/zh_seed_tasks.json)同上，利用text-davinci-003得到Response，相比于0.5M数据集，作者进行了数据清洗：去掉了一些质量不高的数据，例如自称`GPT模型`的数据、由于input不完善导致模型无法回答的数据，以及指令是中文但input或target是英文的数据。|[BELLE](https://github.com/LianjiaTech/BELLE)|
|[BelleGroup/school_math_0.25M](https://huggingface.co/datasets/BelleGroup/school_math_0.25M)|0.25M|中文数学题数据，包含解题过程，由ChatGPT产生|[BELLE](https://github.com/LianjiaTech/BELLE)|
|[BelleGroup/multiturn_chat_0.8M](https://huggingface.co/datasets/BelleGroup/multiturn_chat_0.8M)|0.8M|用户与助手的多轮对话，由ChatGPT产生|[BELLE](https://github.com/LianjiaTech/BELLE)|
|[BelleGroup/generated_chat_0.4M](https://huggingface.co/datasets/BelleGroup/generated_chat_0.4M)|0.4M|个性化角色对话数据，包含角色介绍，由ChatGPT产生|[BELLE](https://github.com/LianjiaTech/BELLE)|
|[BelleGroup/train_2M_CN](https://huggingface.co/datasets/BelleGroup/train_2M_CN)|2M|中文指令数据，由ChatGPT产生|[BELLE](https://github.com/LianjiaTech/BELLE)|
