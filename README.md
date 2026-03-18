# DeFocus Blur Plots

A lightweight experimental notebook for evaluating blur-aware image enhancement in object detection pipelines. The project applies blur simulation, adaptive sharpening, and blur estimation before passing images to a YOLOv8n detector, then visualizes comparative results through detection outputs and performance plots.

## Overview

This repository contains a notebook that supports the experimental visualization pipeline for blur-aware object detection. The workflow focuses on the following steps:

- load a pretrained **YOLOv8n** detector
- simulate blurred inputs using Gaussian blur
- enhance degraded images using lightweight sharpening operations
- estimate blur severity using the **variance of Laplacian**
- compare restored or enhanced images through detection overlays
- generate plots for:
  - detection performance across blur levels
  - **mAP** comparison across methods
  - **BRI** trends across blur levels
  - detector-wise performance comparison before and after enhancement

The notebook is intended for research visualization, comparative analysis, and rapid prototyping.

## Features

- Pretrained **YOLOv8n**-based object detection
- Blur simulation with Gaussian kernels
- Lightweight enhancement pipeline using:
  - **Unsharp Masking**
  - **Laplacian Edge Boosting**
- Blur-level estimation using Laplacian variance
- Comparative plotting for:
  - mAP under different blur settings
  - BRI robustness curves
  - detector comparison under blurred and enhanced conditions
- Figure generation for manuscript and report preparation

## Method Pipeline

The implemented workflow follows this sequence:

1. Load an input image
2. Apply synthetic blur
3. Estimate blur severity
4. Apply sharpening-based enhancement
5. Run object detection using YOLOv8n
6. Visualize detection outputs
7. Plot comparative performance metrics

## Repository Contents

```bash
DeFocus_Blur.ipynb

## Requirements

Install the required dependencies before running the notebook:
pip install ultralytics opencv-python matplotlib numpy

The notebook includes code for:

detector initialization, blur generation, sharpening functions, blur-level estimation, image visualization, plot generation for comparative analysis
