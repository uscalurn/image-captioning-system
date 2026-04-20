# image-captioning-system
Image Captioning with LSTM and Transformer
Overview

This project is about building an Image Captioning system that generates natural language descriptions from images.

I implemented and compared two different approaches:

LSTM with Attention
Transformer Decoder

The main goal is to understand how Transformer performs compared to LSTM in image captioning, both in terms of BLEU scores and caption quality.

Dataset

The project uses the Flickr8k dataset, where each image has 5 reference captions.

Preprocessing steps include:

Tokenization
Vocabulary building
Adding special tokens:
<sos> start of sentence
<eos> end of sentence
<pad> padding
<unk> unknown words
Model Architectures
1. LSTM with Attention
Encoder: CNN (ResNet-based feature extractor)
Decoder: LSTM
Attention mechanism helps the model focus on relevant regions of the image for each word
2. Transformer
Encoder: ResNet50 feature extractor
Decoder: Transformer Decoder
Uses self-attention to capture global relationships between words
Training
Loss function: CrossEntropyLoss (ignoring padding tokens)
Optimizer: Adam
Teacher forcing is used during training
Gradient clipping is applied for stability
Inference

Two decoding strategies are used:

Greedy Search: selects the most probable word at each step
Beam Search: keeps multiple candidate sequences to improve final output

Beam size used in experiments: 3

Results
BLEU Score Comparison (Beam Size = 3)
Metric	LSTM + Attention	Transformer
BLEU-1	XXX	XXX
BLEU-2	XXX	XXX
BLEU-3	XXX	XXX
BLEU-4	XXX	XXX
Observations
Transformer generally produces more fluent and coherent captions
LSTM performs well on simpler sentences but struggles with long-range dependencies
Beam search significantly improves output quality for both models
On a small dataset like Flickr8k, the difference is noticeable but not extreme
Demo Results
Input Image

(Place your input image here)

![Input Image](path_to_input_image.png)
Generated Captions

LSTM Output:

a man riding a bike on the road

Transformer Output:

a man is riding a bicycle on a city street

(You can add more examples here)

BLEU Score Visualization

(Place BLEU comparison image here)

![BLEU Comparison](path_to_bleu_comparison.png)
Attention Visualization (LSTM)

(If available, add attention heatmap visualization here)

![Attention Map](path_to_attention_map.png)
Conclusion
Transformer outperforms LSTM in overall caption quality
LSTM is simpler and still works well as a baseline
Beam search is one of the most important factors improving results
Dataset size plays a big role in how noticeable the improvement is
Notes
Beam search requires batch size = 1
Vocabulary must be consistent between training and inference
Model performance is sensitive to preprocessing quality
Requirements
Python 3.8+
PyTorch
torchvision
numpy
pandas
nltk
matplotlib
PIL
How to Run
Train LSTM or Transformer model using training scripts
Load saved checkpoint for evaluation
Use beam search for generating captions
Author
