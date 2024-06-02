# Fine-Tuning-Meta-Llama2
Dataset: https://huggingface.co/datasets/timdettmers/openassistant-guanaco

- Here, I have fine tuned Meta LLAMA 2 model (Llama-2-7b-chat-hf) with hugging face openassistant-guanaco dataset. 
- We have freesed most of the 7billion parameters of Llama2 models and hence, this fine tuning was possible. 
- Fine Tuning was performed using parameter efficient Transfer Learning method called LoRA (Low-Rank Adaptation of Large Language Models).
- Just to understand how the fine tuned model performs, we are only using 1000 samples of the given dataset to fine tune the model.
- The hyperparameters which I will be using for LORA is rank of 64 with a scaling parameter of 16.


