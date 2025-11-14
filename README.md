# Multi-Lead ECG Classification Using Ensemble Deep Learning

This project implements a systematic comparison of deep learning approaches for automated cardiac arrhythmia classification on the PTB-XL dataset. We progressively evaluate three CNN architectures: single-lead baseline, multi-lead processing, and ensemble learning to demonstrate the importance of spatial information and model diversity in ECG diagnosis.

The single-lead CNN (Lead II only) achieves F1-score of 0.5697. The multi-lead CNN processes all 12 ECG leads simultaneously through a shared convolutional encoder, improving performance to 0.6907 (+21.2%). An ensemble of three independently trained multi-lead models further boosts F1 to 0.7108 (+2.9%), achieving competitive results with state-of-the-art methods. The study classifies five diagnostic categories: normal rhythm (NORM), myocardial infarction (MI), ST/T changes (STTC), conduction disturbances (CD), and hypertrophy (HYP) across 21,799 12-lead ECG recordings. Our systematic analysis quantifies that multi-lead spatial information contributes 86% of performance gains, with ensemble learning providing the remaining 14% through variance reduction. Implemented in PyTorch using the official PTB-XL 100 Hz dataset with proper train/validation/test splits.

## Results
- **Single-Lead CNN**: F1 = 0.5697
- **Multi-Lead CNN**: F1 = 0.6907 (+21.2%)
- **Ensemble (3 models)**: F1 = 0.7108 (+2.9%)

