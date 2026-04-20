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

<img width="595" height="367" alt="image" src="https://github.com/user-attachments/assets/2879ec28-855f-49bb-b954-a62c76afabe2" />


---

## Demo

### Input Image
<img width="1000" height="667" alt="anhtest" src="https://github.com/user-attachments/assets/9282e55f-21fa-4345-a0c8-5f94c5daf4f6" />



---

### Output Caption


<img width="1468" height="891" alt="image" src="https://github.com/user-attachments/assets/f41c553b-a23c-40f8-9be4-13fc7d95481a" />


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
Nguyen Minh Nhan.
