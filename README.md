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
* Evaluation: We compare the generated and actual text, then conduct human studies to test the indistinguishability of LLM-generated text.
