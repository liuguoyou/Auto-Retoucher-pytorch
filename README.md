# Auto-Retoucher(ART)--A Framework for Background Replacement and Foreground adjustment
Given someone's photo, generates a new image with best matching background, and find the best spatial location and scale.

A PyTorch implementation of ART framework. Our paper is available here [PDF](resource/CV_paper.pdf)

## Abstract
Replacing the background and simultaneously adjusting foreground objects is a challenging task in image editing. Current techniques for generating such images are heavily relied on user interactions with image editing softwares, which is a tedious job for professional retouchers. Some exciting progress on image editing has been made to ease their workload. However, few models focused on guarantee the semantic consistency between the foreground and background. To solve this problem, we propose a   framework —— ART(Auto-Retoucher)，to generate images with sufficient semantic and spatial consistency from a given image. Inputs are first processed by semantic matting and scene parsing modules, then a multi-task verifier model will give two confidence scores for the current matching and foreground location. We demonstrate that our jointly optimized verifier model successfully guides the foreground adjustment and improves the global visual consistency.

### Example foreground images:

![resource/test_1.png](resource/test_1.png)
![resource/test_2.png](resource/test_2.png)

### Output Images:

The backgrounds are selected from gallery, with best content-level consistency.

![resource/result1.png](resource/demo2.png)
![resource/result1.png](resource/result1.png)

### moving sequence:
Adjustment procedure guided by model's gradient. 

Fg moves from a random initial location to a plausible position

![resource/result1_seq.png](resource/moving_sequence1.jpg)
![resource/result2_seq.png](resource/moving_sequence2.jpg)

## Framework:
![](resource/pipeline.jpg =100x100)


## Training:

```
python train.py
```

## Inference:

```
python Inference.py
```
