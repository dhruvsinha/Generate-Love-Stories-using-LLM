# Generate Love Stories using Large Language Models

CHRISTOPHER T. KANG and DHRUV SINHA, The University of Chicago, USA

## Introduction

Large Language Models (LLMs) are lauded for their ability to consume massive volumes of text. This ability is pertinent when
consuming corpora containing long-form text, e.g., books, scientific papers, or when generating long-form text. However, specific
genres — like poetry — are defined by their brevity. In this work, we train GPT2 Neo via prompt engineering and fine-tuning on the New
York Times’ Tiny Love Stories. Human evaluation suggests that prompt engineered stories are indistinguishable from human-written
stories. We explore what this implies for the capabilities of LLMs in concise, emotion-rich regimes. 

## Task and Methodology

In our text generation task, we provide the model with a real NYT Tiny Love Stories title and seek to generate a realistic
love story within 100 words. To achieve this generation, we proceed with the project in three phases:

* Gather data: We scrape the title and text of Tiny Love Stories, then perform a qualitative analysis of the
obtained stories.
* Training: We test two training strategies, prompt engineering and fine-tuning, and analyze their performance
when generating text.
* Evaluation: We compare the generated and actual text, then conduct human studies to test the indistinguishability of LLM-generated text.

In this summary document, we will briefly describe the training and evaluation part of this project. Please refer to the paper attached in the repository to read more about each component of this project. 

## Training
Because our task is text generation, we choose to use the GPT family of models. In particular, the GPT Neo models are
well-known and have been optimized. We consider two of the newer models, GPT2-Neo 2.7B [2] and GPT2-NeoX 20B
[1]. Using these two models, we test two strategies to generate content: Prompt Engineering and Fine Tuning. The results from fine-tuned model were incomprehensible. We have discussed the potential reasons in the paper. Here, we have discussed the Prompt Engineering approach briefly:

Our prompt engineering approach is intuitive " we provide the following prompt structure to the model:
Title: [[ Example title ]]
Story: [[ Example story]]

Title: [[ Test title ]]
Story:

During generation, we randomly select an example title/story pair from the training dataset. We then requested the
model generate between 100-200 tokens and truncated any excess text.
While other applications would find this prompt approach challenging due to the context limit, the text length
restriction imposed by the dataset makes prompt engineering feasible. It is challenging to think of examples where 100
word stories would exceed 1024 tokens, even at a character-level tokenization.
When using the 20B model, our generation consistently generated syntactically correct stories. Furthermore, the
length of stories generated often mimicked the input story’s length, thus implicitly approximating the NYT length
requirement.




