##  Topic 2: Effect of Stride & Padding on CNN Feature Extraction

**Dataset:** MNIST  
**Objective:** To understand how stride and padding influence spatial resolution, feature extraction, and classification accuracy in Convolutional Neural Networks (CNNs).

### Configurations Compared
We trained four CNNs with identical architectures while varying only stride and padding:

| Model | Stride | Padding | Notes |
|-------|--------|----------|-------|
| Model A | 1 | SAME | Best detail preservation |
| Model B | 2 | SAME | Downsamples feature maps |
| Model C | 1 | VALID | Border information lost |
| Model D | 2 | VALID | Most aggressive reduction |

###  Key Findings
- **Stride 1 + SAME** produced the best accuracy and cleanest feature maps.  
- **VALID padding** shrinks outputs, removing border details that are important for digit recognition.  
- **Stride 2 models** lose fine-grained features and perform worse.  
- Feature maps show how SAME padding preserves digit structure, while VALID padding loses edges.

###  Visualisations Included
- `stride_padding_accuracy.png` — Validation accuracy comparison  
- `feature_maps_stride1_same.png` — Feature map visualisation  
- `sample_mnist_stride_padding.png` — Input sample used for analysis  

###  Files for Topic 2
- `topic2_notebook.ipynb` — Full training code with explanations  
- `topic2_report.pdf` — Professional written report (~2000 words)  
- Saved figures used in the report  

### Summary
This topic demonstrates that **stride and padding are not cosmetic choices**; they fundamentally alter how CNNs perceive spatial information. SAME padding and small strides retain the most visual detail, leading to stronger classification performance on MNIST.
