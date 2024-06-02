# Fine-Tuning-Meta-Llama2
Dataset: https://huggingface.co/datasets/timdettmers/openassistant-guanaco

- Here, I have fine-tuned the Meta LLAMA 2 model (Llama-2-7b-chat-hf) with the hugging face open assistant-guanaco dataset. 
- We have frozen most of the 7 billion parameters of Llama2 models and hence, this fine-tuning was possible. 
- Fine Tuning was performed using a parameter efficient Transfer Learning method called LoRA (Low-Rank Adaptation of Large Language Models).
- Just to understand how the fine-tuned model performs, we are only using 1000 samples of the given dataset to fine-tune the model.
- The hyperparameters that I will be using for LORA is a rank of 64 with a scaling parameter of 16.
- The training was done for 1 epoch, because of the huge memory consumption.
- The same procedure will be performed while training on GPUs. We will use smaller batch sizes and a large number of epochs to improve the performance of the model on the given dataset.

- Veriosn of PEFT: 0.4.0
The following `bitsandbytes` quantization config was used during training:
- load_in_8bit: False
- load_in_4bit: True
- llm_int8_threshold: 6.0
- llm_int8_skip_modules: None
- llm_int8_enable_fp32_cpu_offload: False
- llm_int8_has_fp16_weight: False
- bnb_4bit_quant_type: nf4
- bnb_4bit_use_double_quant: False
- bnb_4bit_compute_dtype: float16





