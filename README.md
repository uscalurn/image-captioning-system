# Image Captioning (LSTM vs Transformer)

## Overview
This project builds an image captioning system that generates natural language descriptions for images.

Two models are implemented and compared:
- LSTM with Attention
- Transformer Decoder

---

## Dataset
Flickr8k dataset (each image has 5 captions).

Preprocessing:
- Tokenization
- Vocabulary building
- Special tokens: `<sos>`, `<eos>`, `<pad>`, `<unk>`

---

## Models

### LSTM + Attention
- CNN encoder (ResNet)
- LSTM decoder
- Attention mechanism over image features

### Transformer
- ResNet50 encoder
- Transformer decoder with self-attention

---

## Training
- Loss: CrossEntropyLoss (ignore padding)
- Optimizer: Adam
- Teacher forcing
- Gradient clipping

---

## Inference
- Greedy search
- Beam search (beam size = 3)

---

## Results

### BLEU Score Comparison

| Metric | LSTM | Transformer |
|--------|------|-------------|
| BLEU-1 | XXX  | XXX         |
| BLEU-2 | XXX  | XXX         |
| BLEU-3 | XXX  | XXX         |
| BLEU-4 | XXX  | XXX         |

---

## Demo

### Input Image
(Insert input image here)

![input](path_to_input_image.png)

---

### Output Caption

LSTM:
"a man riding a bike on the road"

Transformer:
"a man is riding a bicycle on a street"

---

### BLEU Comparison Chart
(Insert chart here)

![bleu](path_to_bleu_chart.png)

---

## Conclusion
Transformer performs better overall in caption quality and BLEU score.  
LSTM is simpler and works well as a baseline.

Beam search improves results for both models.

---

## Requirements
PyTorch, torchvision, numpy, pandas, nltk, matplotlib, PIL

---

## Author
Image captioning project using LSTM and Transformer for deep learning practice.
