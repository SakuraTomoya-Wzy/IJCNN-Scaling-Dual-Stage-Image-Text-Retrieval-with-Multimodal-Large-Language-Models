# IJCNN-Scaling-Dual-Stage-Image-Text-Retrieval-with-Multimodal-Large-Language-Models
The code of IJCNN paper named Scaling Dual Stage Image-Text Retrieval with Multimodal Large Language Models

由于英文分词的问题，加上我们使用了Qwen-VL，Qwen-VL建议使用中文的Prompt。

```
query = tokenizer.from_list_format([
    {'image': './cat.png'}, # Either a local path or an url
    {'text': """上面这个图用一个中文词来表达是：猫。"""},
    {'image': file_path}, # Either a local path or an url
    {'text': """上面这个图用一个中文词来表达是："""},
])
```

建议试试[InternVL](https://github.com/OpenGVLab/InternVL)，他等于是在预训练阶段就使用了我们的任务驱动的微调目标。
