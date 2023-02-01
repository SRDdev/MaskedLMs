# <img src="https://cdn-icons-png.flaticon.com/32/3269/3269817.png"> MaskedLM

MaskedLM is a pre-training technique used in Natural Language Processing (NLP) for deep-learning models like Transformers. It is a variant of language modeling where a portion of the input text is masked, and the model is trained to predict the masked tokens based on the context provided by the unmasked tokens.

## Models

1. [EngMaskedLM](https://github.com/SRDdev/MaskedLMs/tree/master/EngMaskedLM) 

2. [HingMaskedLM](https://github.com/SRDdev/MaskedLMs/tree/master/HingMaskedLM)

## Inference
Load model
```python
from transformers import AutoTokenizer, AutoModelForMaskedLM, 

tokenizer = AutoTokenizer.from_pretrained("SRDdev/HingMaskedLM")
model = AutoModelForMaskedLM.from_pretrained("SRDdev/HingMaskedLM")
```
Build pipeline
```python
from transformers import pipeline

fill = pipeline('fill-mask', model=model, tokenizer=tokenizer)
fill(f'please {fill.tokenizer.mask_token} ko cancel kardo')
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
Please make sure to update tests as appropriate.

## Citations
```
@citation{ HingMaskedLM,
  author = {Shreyas Dixit},
  year = {2023},
  url = {https://huggingface.co/SRDdev/HingMaskedLM}
}
```

