# Mask2Former — Intro Semantic Segmentation Notebook

This notebook explores transformer-based semantic segmentation using Mask2Former in the context of autonomous vehicle perception systems.

## Goals

- Run Mask2Former on a street-scene image
- Generate semantic segmentation maps
- Compare semantic segmentation with SAM automatic mask generation
- Measure inference latency and GPU memory usage
- Document observations relevant to autonomous vehicle perception

---

## Why Mask2Former?

While Segment Anything (SAM) produces strong generic region masks, those masks are not inherently semantic. Autonomous vehicles require not only object boundaries, but also semantic understanding of scene regions such as:

- road
- sidewalk
- vehicle
- pedestrian
- traffic sign
- building

Mask2Former combines transformer-based scene understanding with semantic segmentation and is therefore more aligned with real-world perception systems.

---

## Background

Mask2Former uses a transformer-based architecture for segmentation. Unlike traditional CNN-only approaches, transformer architectures enable global contextual reasoning across an image, helping improve scene understanding and object coherence.

This notebook uses a Cityscapes-trained Mask2Former checkpoint to explore semantic segmentation on urban driving scenes.

---

## Topics Explored

- Semantic segmentation
- Transformer-based vision models
- Scene understanding
- Segmentation visualization
- Inference latency
- GPU memory usage
- Autonomous vehicle perception constraints

---

## Autonomous Vehicle Relevance

Autonomous vehicle perception systems additionally require:

- Processing continuous video streams across time
- Low-latency, real-time inference
- Object tracking and trajectory prediction
- Semantic understanding of regions, not just region boundaries
- Integration across multi-camera and multi-sensor perception stacks
- Operation under constrained onboard compute and memory resources
- High levels of safety, robustness, and reliability

---

## Open in Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chrishpaul/cv-research-lab/blob/main/notebooks/mask2former-intro/mask2former_inference_colab.ipynb)

---

## Suggested Next Steps

- Compare Mask2Former output against SAM on the same image
- Explore panoptic segmentation
- Test on dashcam or KITTI images
- Measure performance across different model sizes
- Explore video segmentation and tracking
- Investigate temporal consistency across frames

---

## References

- Mask2Former
- Cityscapes Dataset
- Segment Anything (SAM)
- Hugging Face Transformers
