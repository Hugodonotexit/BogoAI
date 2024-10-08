# BogoAI Model

BogoAI is a conceptual model inspired by Bogo Sort and the infinite monkey theorem. It generates random outputs and is not intended for practical use. It has a time complexity og O(n!) were as n is the length of the output text;

## Model Details

- **Vocabulary Size**: 152064
- **Tokenizer**: Qwen/Qwen2.5-72B-Instruct

## Installation

To use this model, install the required libraries:

```bash
pip install transformers huggingface_hub
```

## Usage

Here's how to load and use the BogoAI model:

```python
import torch
from transformers import AutoTokenizer, AutoModel

# Load tokenizer and model
tokenizer = AutoTokenizer.from_pretrained("Hugo0123/BogoAI")
model = AutoModel.from_pretrained("Hugo0123/BogoAI")

# Example input
input_text = "Example input text"
input_ids = tokenizer.encode(input_text, return_tensors='pt')

# Generate random output
output_ids = model(input_ids=input_ids)
output_text = tokenizer.decode(output_ids[0], skip_special_tokens=True)
print("Output:", output_text)
```

## License

MIT