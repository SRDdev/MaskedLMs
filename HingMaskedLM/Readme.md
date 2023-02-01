
### HingMaskedLM
This is a BERT model trained for Masked Language Modeling for Hinglish Data.

### Dataset
Hinglish-Top [Dataset](https://huggingface.co/datasets/WillHeld/hinglish_top) columns
- en_query
- cs_query
- en_parse 
- cs_parse 
- domain 

### Training
|Epoch|Loss|
|:--:|:--:|
|1	|0.0465|
|2	|0.0262|
|3	|0.0116|
|4	|0.00385|
|5	|0.0103|
|6	|0.00738|
|7	|0.00892|
|8	|0.00379|
|9	|0.00126|
|10	|0.000684|


### Inference 
```python
from transformers import AutoTokenizer, AutoModelForMaskedLM, pipeline

tokenizer = AutoTokenizer.from_pretrained("SRDdev/HingMaskedLM")

model = AutoModelForMaskedLM.from_pretrained("SRDdev/HingMaskedLM")

fill = pipeline('fill-mask', model=model, tokenizer=tokenizer)
```
```python
fill(f'please {fill.tokenizer.mask_token} ko cancel kardo')
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