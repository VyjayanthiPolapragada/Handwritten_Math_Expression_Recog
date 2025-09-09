# Handwritten Mathematical Expression Recognition

A deep learning pipeline to recognize and convert handwritten mathematical expressions into LaTeX markup using CNNs, Transformers, and hybrid architectures. This project demonstrates the full workflow from raw InkML files to model training, evaluation, and beam search decoding.

## Features

- **InkML to Image Conversion**: Converts handwritten InkML stroke data into PNG images for model input.  
- **Multiple Model Architectures**:
  - CNN + LSTM  
  - ResNet + Transformer  
  - ResNet + Posformer (best performing)  
- **Evaluation Metrics**: Token-level accuracy, exact match accuracy, Character Error Rate (CER), and BLEU score.  
- **Beam Search Decoding**: Generates LaTeX sequences from model predictions.  


## Model Performance

| Model                | Token-Level Accuracy (%) | Exact Match Accuracy (%) | Character Error Rate (CER) | BLEU Score |
|:---------------------|------------------------:|------------------------:|---------------------------:|------------:|
| CNN + LSTM           | 69.18                   | 30.73                   | 0.4314                     | 0.3312      |
| ResNet + Transformer | 74.12                   | 31.37                   | 0.4131                     | 0.4223      |
| ResNet + Posformer   | 81.07                   | 35.07                   | 0.2372                     | 0.5944      |

*The ResNet + Posformer model achieves the best performance across all metrics.*


## Getting Started

### Requirements

- Python 3.8+  
- PyTorch  
- Matplotlib  
- Numpy  
- (Optional) GPU for faster training  

## Dataset

- **Source**: InkML files from this [Link](https://www.kaggle.com/datasets/rtatman/handwritten-mathematical-expressions/data)
- **Preprocessing**: InkML stroke files are converted to PNG images for model training.

## Conclusion

- This project demonstrates a complete pipeline for handwritten mathematical expression recognition:

- Data preprocessing: InkML stroke data is converted into images.

- Model training: Multiple architectures (CNN+LSTM, ResNet+Transformer, ResNet+Posformer) are evaluated.

- Evaluation: Models are compared using token-level accuracy, exact match, CER, and BLEU scores.

- Beam search decoding: Generates accurate LaTeX sequences.

The ResNet + Posformer model achieves the highest performance, showing the effectiveness of combining convolutional feature extraction with transformer-based sequence modeling. The pipeline can be further improved with data augmentation or larger datasets.

