# Fine Tuning the Deepset/roberta-base-squad2 on custom dataset using Simple Transformers

RoBERTa-base fine-tuned on SQuAD 2.0 is a powerful question-answering model built on the RoBERTa architecture, specifically trained for tasks that require extracting answers from a given context. Here’s a breakdown:

### RoBERTa Architecture
- **RoBERTa (Robustly optimized BERT approach)** is an enhanced version of BERT (Bidirectional Encoder Representations from Transformers). It was developed by Facebook AI and is designed to improve upon BERT by tweaking the training process:
  - **More Data:** RoBERTa was trained on a significantly larger dataset compared to BERT, including Common Crawl data.
  - **Longer Training:** It was trained for more iterations, resulting in a more robust model.
  - **Dynamic Masking:** Unlike BERT, RoBERTa dynamically changes the masked tokens during training, rather than keeping them static.
  - **No Next Sentence Prediction (NSP):** RoBERTa omits the NSP task, which BERT uses, arguing that it might not be necessary for performance improvements.

### SQuAD 2.0 Dataset
- **SQuAD 2.0 (Stanford Question Answering Dataset version 2.0)** combines the original SQuAD 1.1 with over 50,000 unanswerable questions written adversarially by crowd workers to look similar to answerable ones. 
- **Challenge:** The model must not only answer questions based on the context but also determine when no answer is possible.
- **Evaluation:** The model is evaluated on its ability to correctly predict when a question is unanswerable, in addition to providing correct answers for answerable questions.

### RoBERTa-base SQuAD 2.0 Model
- **RoBERTa-base** refers to the "base" version of the RoBERTa model, which has 12 layers (transformer blocks), 768 hidden units, and 12 attention heads, totaling around 125 million parameters.
- **Fine-tuning:** RoBERTa-base has been fine-tuned on the SQuAD 2.0 dataset to perform question-answering tasks. This fine-tuning involves adjusting the pre-trained model's parameters specifically for the SQuAD 2.0 task, enabling it to not only extract answers from a given context but also recognize when no valid answer exists.

### Model Performance
- **Accuracy:** RoBERTa models, especially after fine-tuning on SQuAD 2.0, generally outperform BERT models in terms of both exact match (EM) and F1 score metrics.
- **Capabilities:** The fine-tuned RoBERTa-base model can handle a wide range of question-answering scenarios, including dealing with ambiguous or misleading questions where no answer is present in the context.

### Use Cases
- **Information Retrieval:** Can be used in systems that need to extract precise information from large datasets.
- **Chatbots and Virtual Assistants:** Enhances the ability of AI-powered assistants to provide accurate responses to user queries.
- **Research and Analysis:** Useful in academic or professional settings where detailed answers are needed from text-heavy documents.

In summary, RoBERTa-base fine-tuned on SQuAD 2.0 is a highly capable model for question-answering tasks, balancing the challenges of finding exact answers while also identifying when no answer is present.

## Install the Dependencies

``` bash
pip install -r requirements.txt

```
## Custom Dataset

Use the Custom Dataset ( sampledataset.json) or create on of similar format.

