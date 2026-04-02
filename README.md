# 🤗 Hugging Face Learning Journey

This repository documents my step-by-step learning of Hugging Face tools for applied machine learning, with a focus on **text data and real-world workflows**.

The goal is to build a clear understanding of the full pipeline:

data → preprocessing → training → evaluation → sharing → application


### 01 - Loading Data

What this covers:

loading datasets using load_dataset
accessing train/test splits
initial dataset exploration

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1duMcbGLoQ8qvtohJAcshDo2nawSeDjme?usp=sharing) 


### 02 - Inspect Dataset

What this covers:

inspecting samples and features
understanding dataset structure
checking dataset size and label distribution

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KrS-ExjGqpYtJTVSG-7oV_VdeNNF_-4U?usp=sharing) 


### 03 - Preprocessing
This notebook covers:
- general preprocessing such as filtering and text transformation
- text preprocessing for transformers
- tokenization with a matching pretrained tokenizer
- preparing the dataset for PyTorch

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16K3EyhLdsuEIcLjlMOIpdvO78QQTiZLw?usp=sharing) 

### 04 - Fine-Tuning With Trainer API
This notebook continues after preprocessing and shows how to:
- load a pretrained text classification model
- define training settings with `TrainingArguments`
- use `Trainer` to fine-tune the model
- evaluate performance with accuracy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1-PbjWmTd06UDBX1adcAJwcJkV-qVpsdd?usp=sharing)

### 05 - Custom Training Loop
This notebook explains how text classification training works without the Trainer API:
- prepare tokenized data for PyTorch
- create DataLoaders
- define optimizer and scheduler
- run a manual training loop
- evaluate the model

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1iSDftsbvRxin-VwkMXxRFJnz-AaIz70R?usp=sharing)

### 06 - Understanding Learning Curves
This notebook explains how to interpret:
- training and validation loss
- validation accuracy
- healthy learning curves
- overfitting
- underfitting
- unstable training

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1VvmmF0yqyzptjCnQcfAfjMivZql0b--E?usp=sharing)


### 07 - Sharing Models

Use and share models via the Hugging Face Hub.
- loading pretrained models
- saving models locally
- pushing models to the Hub
- model cards

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1m63geXJGRIYByIj2Hs92bayjqHArAQ0s?usp=sharing)

### 08 - Classical NLP Tasks
This notebook covers the most practical classical NLP tasks that form the foundation of modern language models:

- token classification
- question answering
- summarization
- translation

For each task, I included:
- the main idea
- a small practical example
- the key preprocessing concept
- the common evaluation metric
- a short summary of what I learned

#### Main takeaways
- token classification requires label alignment with subword tokens
- extractive QA requires mapping answer spans from characters to tokens
- summarization typically uses encoder-decoder models and ROUGE
- translation uses sequence-to-sequence models and SacreBLEU

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/125NjVTrImNsjknN-NJ77TyRuRtuBW0Mr?usp=sharing)


### 9 - Supervised Fine-Tuning and LoRA
This notebook covers the practical workflow for adapting a pretrained language model into an assistant-style model.

#### Topics covered
- chat templates
- supervised fine-tuning (SFT)
- LoRA
- evaluation after fine-tuning

#### Main takeaways
- instruct models require the correct chat template
- SFT is useful only when prompting is not enough
- LoRA makes fine-tuning much more memory-efficient
- evaluation should include both metrics and qualitative checks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XWXy8U1KArg9lvapUx6J4dNMYoE65prf?usp=sharing)
