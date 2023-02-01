
### SRDberta
<a href="https://huggingface.co/SRDdev/SRDBerta" target="blank">
<img alt="Huggingface" src="https://img.shields.io/badge/%F0%9F%A4%97-Huggingface-yellow">
</a>

This is Transformer Model trained for Masked Language Modeling for small English Data.

### Dataset
Hinglish-Top [Dataset](https://huggingface.co/datasets/WillHeld/hinglish_top)


### Training
|Epochs|Train Loss|
|:------:|:----------:|
|4th   |   0.251 |

The model was trained only for 4 epochs due to the GPU limitations. The model will give far better results with 10 epochs

### Inference 
```python
from transformers import AutoTokenizer, AutoModelForMaskedLM, pipeline

tokenizer = AutoTokenizer.from_pretrained("SRDdev/SRDBerta")

model = AutoModelForMaskedLM.from_pretrained("SRDdev/SRDBerta")

fill = pipeline('fill-mask', model='SRDberta', tokenizer='SRDberta')
```
```python
fill_mask = fill.tokenizer.mask_token
fill(f'Aap {fill_mask} ho?')
```

### Citation
Author: @[SRDdev](https://huggingface.co/SRDdev)
```
Name : Shreyas Dixit
framework : Pytorch
Year: Jan 2023
Pipeline : fill-mask
Github : https://github.com/SRDdev
LinkedIn : https://www.linkedin.com/in/srddev/ 
```
