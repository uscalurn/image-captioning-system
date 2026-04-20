Image Captioning (LSTM vs Transformer)
Overview

This project builds an image captioning system that generates natural language descriptions from images.

Two models are implemented and compared:

LSTM with Attention
Transformer Decoder
Dataset

Flickr8k dataset, each image has 5 captions.

Preprocessing includes:

Tokenization
Vocabulary building
Special tokens: <sos>, <eos>, <pad>, <unk>
Models
LSTM + Attention
CNN encoder (ResNet)
LSTM decoder
Attention over image features
Transformer
ResNet50 encoder
Transformer decoder with self-attention
Training
Loss: CrossEntropyLoss (ignore padding)
Optimizer: Adam
Teacher forcing used
Gradient clipping applied
Inference
Greedy search
Beam search (beam size = 3)
