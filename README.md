Ensemble Models for Robust Skin Cancer Detection with 3D Total-Body Photographs  

**Authors:** Yuehan He, Chunyu Li, Xiaoqian Zhou, Zongwei Huang, Mira Parikh  
**Date:** April 30, 2025  



Overview 
Skin cancer, particularly melanoma, is among the deadliest cancers worldwide. Early detection significantly improves patient outcomes, but traditional diagnostics can be subjective and inaccessible.  
This project explores **ensemble machine learning approaches** that combine dermoscopic image analysis with patient metadata to improve skin cancer detection.  



Methods 
We built a **multimodal ensemble framework** with two main components:  

1. Image-based CNNs  
   - ResNet50  
   - EfficientNet-B0  
   - DenseNet121  

2. Metadata-based Gradient Boosting Models
   - XGBoost  
   - LightGBM  
   - CatBoost  

Training & Optimization  
- Hyperparameter tuning with **Optuna**  
- Data augmentation to address class imbalance (flips, rotations, color adjustments, external malignant samples)  
- Weighted binary cross-entropy loss for CNNs  

Ensemble Strategies  
- Average Ensemble  
- Weighted Ensemble  
- Stacked Ensemble (Logistic Regression, Random Forest)  



Results
Evaluation metric: **Partial AUC (pAUC) above 80% TPR (to emphasize high-sensitivity predictions in clinical use).  

- Best performance: Weighted Ensemble integrating CNN + Gradient Boosting models  
- Key insight: Metadata-based models often outperformed image-only models, highlighting the importance of multimodal integration  



Takeaways
- Multimodal ensemble models improve robustness and sensitivity in melanoma detection  
- Weighted ensembles were most effective, outperforming stacking methods  
- Metadata provided crucial complementary signals to image-based classifiers  



Future Work
- Explore attention-based multimodal networks to better capture interactions between image and metadata features  
- Investigate neural network meta-learners for stacking to improve over Random Forest or Logistic Regression baselines  


