# AI-Powered Smart Agriculture and Plant Health Intelligence

**Status: v0.1 (Week 1). Work in progress. No model results yet.**

## Problem
Plant diseases reduce crop yield, and early identification helps farmers act sooner.
This project builds a model that classifies supported plant disease/health categories
from leaf images, tests whether it works on images from a different source, and
presents the result in a web application with clearly limited environmental context.

## Scope
- Train and compare a small CNN, EfficientNet-B0 and ResNet-50 on PlantVillage.
- Evaluate externally on compatible PlantDoc labels (never used for tuning).
- Report accuracy, macro F1, per-class recall, confusion matrices, latency and model size.
- Build a Streamlit app with upload validation and uncertainty warnings.
- Show public NASA POWER weather data with a transparent, rule-based advisory.

## Out of scope (for now)
- Sensors or IoT hardware.
- Exact irrigation amounts from weather alone.
- Merging dataset labels without a documented mapping.
- Claiming field reliability from controlled-dataset scores.

## Planned modules
1. Data pipeline and splits
2. Model training and comparison
3. Evaluation and error analysis
4. Calibration and uncertainty
5. Inference module
6. Environmental data and advisory
7. Streamlit application

## Tools
Google Colab, PyTorch, Torchvision, scikit-learn, Pandas, Matplotlib, Streamlit.

## Disclaimer
Model output is not a definitive diagnosis. No performance numbers are reported yet.
