# Comparative Evaluation of YOLOv8 Variants for Object Detection

This repository presents a controlled comparative study of **YOLOv8 model variants (YOLOv8n and YOLOv8s)** on a custom object detection dataset containing **Dog** and **Duck** classes.

The analysis focuses on **object-scale sensitivity**, **data-split generalization**, **class imbalance**, and **accuracy–efficiency trade-offs**, supported by quantitative metrics and qualitative error analysis.

---

## Dataset
- **Source:** Open Images V7  
- **Classes:**
  - Duck (class 0)
  - Dog (class 1)
- **Annotation format:** YOLOv8
- **Dataset splits:**
  - Train: ~400 images
  - Validation: ~268 images
  - Test: ~399 images

Directory structure used:
data/
images/{train,val,test}
labels/{train,val,test}


---

## Methodology
- Fine-tuned pretrained **YOLOv8n** and **YOLOv8s**
- Identical training settings for fair comparison
- Evaluation on **validation and test splits**
- Conducted:
  - Split-wise performance analysis
  - Object-scale analysis (small vs large objects)
  - Class-wise analysis (Dog vs Duck)
  - Inference speed benchmarking
  - Qualitative error analysis

---

## Key Findings
- YOLOv8n and YOLOv8s show comparable performance across splits
- Object scale has a stronger impact than model capacity
- Duck detection is significantly more challenging due to class imbalance and small object size
- Increasing model size does not improve performance under dataset constraints

---

## How to Run

Install dependencies:
```bash
pip install -r requirements.txt

