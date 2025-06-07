# AI-Based Diabetes Risk Prediction System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Machine Learning](https://img.shields.io/badge/ML-Ensemble%20Learning-green.svg)](https://scikit-learn.org/)

## Overview

A comprehensive machine learning system designed to predict diabetes risk using clinical and lifestyle indicators. This project employs advanced ensemble learning techniques, medical-cost aware optimization, and robust validation frameworks to deliver clinically relevant predictions for early diabetes intervention.

## 🎯 Key Achievements

- **74.68%** Overall Accuracy
- **81.48%** Sensitivity (Recall) - Critical for medical applications
- **81.28%** AUC-ROC Score
- **3.29%** Generalization Gap - Excellent model stability
- **8-Model Ensemble** with optimized voting strategy

## 📊 Dataset Information

| Attribute | Details |
|-----------|---------|
| **Source** | Pima Indians Diabetes Dataset |
| **Sample Size** | 768 patient records |
| **Features** | 8 clinical variables |
| **Target Variable** | Binary diabetes diagnosis (5-year onset) |
| **Population** | Pima Indian women (ages 21+) |

### Clinical Features
- Pregnancies count
- Glucose concentration (2-hour oral glucose tolerance test, mg/dL)
- Blood pressure (diastolic, mm Hg)
- Skin thickness (triceps skinfold, mm)
- Insulin level (2-hour serum insulin, mu U/ml)
- Body Mass Index (BMI, kg/m^2)
- Diabetes pedigree function (genetic risk factor)
- Age (years)

## 🔬 Methodology

### Machine Learning Pipeline
```
Data Preprocessing → Feature Engineering → Feature Selection → Model Training → Ensemble Learning → Validation
```

### Technical Components

#### Feature Engineering & Selection
- **Hybrid Approach**: Recursive Feature Elimination (RFE) + Univariate Statistical Selection
- **Domain Knowledge Integration**: Medical literature-informed feature creation
- **Correlation Analysis**: Multicollinearity detection and resolution

#### Model Development
- **Base Models**: 13 diverse algorithms including tree-based, linear, and distance-based methods
- **Optimization**: Grid Search and Random Search hyperparameter tuning
- **Cost-Sensitive Learning**: Medical-cost aware scoring function
- **Threshold Optimization**: Custom thresholds for clinical decision-making

#### Ensemble Strategy
- **Equal Weight Voting**: Democratic ensemble approach
- **Performance-Weighted**: Accuracy-based model weighting
- **Stability-Weighted**: Cross-validation consistency-based weighting

#### Validation Framework
- **Cross-Validation**: 5-fold Stratified K-Fold
- **Learning Curves**: Training/validation performance analysis
- **Generalization Assessment**: Train-test performance gap analysis

## 📈 Performance Metrics

### Clinical Performance
| Metric | Value | Clinical Significance |
|--------|-------|---------------------|
| **Accuracy** | 74.68% | Overall diagnostic accuracy |
| **Precision (PPV)** | 60.27% | Positive prediction value |
| **Recall (Sensitivity)** | 81.48% | True positive rate (critical for screening) |
| **Specificity** | 71.00% | True negative rate |
| **F1-Score** | 69.29% | Harmonic mean of precision and recall |
| **AUC-ROC** | 81.28% | Area under the ROC curve |

### Risk Assessment
- **False Negative Rate**: 18.52% (10 missed diabetes cases)
- **False Positive Rate**: 29.00% (29 false alarms)
- **Optimal Threshold**: 0.65 (medical-cost optimized)

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8 or higher

### Dependencies Installation
```bash
# Core machine learning libraries
pip install numpy pandas scikit-learn

# Optimization and statistics
pip install scikit-optimize statsmodels

# Visualization and analysis
pip install matplotlib seaborn 

```

### Quick Start
```bash
# Clone the repository
git clone https://github.com/ArthurTechy/AI-Based-Diabetes-Risk-prediction.git
cd AI-Based-Diabetes-Risk-prediction

# Install dependencies
pip install -r requirements.txt

```

## 📁 Project Structure

```
AI-Based-Diabetes-Risk-prediction/
│
├── 📊 data/
│   ├── raw/                    # Original dataset
│   ├── processed/              # Cleaned and engineered features
│   └── external/               # Additional data sources
│
├── 🔬 notebooks/
│   ├── AI_Based_Diabetes_Risk_Prediction.ipynb
│   ├  ├── main_interactive_system
│   ├── Diabetes_AI_Predictive_System_Technical_Report.pdf
│    
├── 🤖 models/
│   ├── base_models/            # Individual trained models
│   ├── ensemble/               # Final ensemble model
│   └── artifacts/              # Model metadata and configs
│
├── 📈 results/
│   ├── figures/                # Visualization outputs
│   ├── reports/                # Performance reports
│   └── logs/                   # Training logs
│
├── 🧪 tests/
│   ├── preprocessor.pkl
│   ├── best_models.pkl
│   └── optimal_threshold.pkl
│
├── 📋 requirements.txt         # Python dependencies
└── 📖 README.md               # This file
```

## 🚀 Usage Examples

### Basic Prediction
```python
main_interactive_system whithin the Notebook
```

## 🏥 Clinical Applications

### Primary Use Cases
- **Risk Screening**: Early identification of high-risk patients
- **Clinical Decision Support**: Automated risk assessment in healthcare workflows
- **Population Health**: Large-scale diabetes risk stratification
- **Research Tool**: Epidemiological studies and clinical trials

### Integration Considerations
- **EHR Compatibility**: Designed for electronic health record integration
- **Real-time Processing**: Optimized for clinical workflow integration
- **Interpretability**: Feature importance and decision explanations available

## 🔬 Model Interpretability

### Feature Importance Analysis
- **Top Predictor**: Pregnancies (primary risk factor)
- **Critical Triad**: Top 3 features contribute 57.4% of predictive power
- **Clinical Relevance**: All selected features align with medical literature

### Decision Explanation
The system provides:
- Individual prediction confidence scores
- Feature contribution analysis
- Risk factor identification
- Actionable clinical insights

## ⚠️ Limitations & Considerations

### Dataset Limitations
- **Population Specificity**: Trained on Pima Indian women only
- **Sample Size**: Limited to 768 records
- **Temporal Scope**: 5-year prediction window
- **Geographic Constraint**: Single population study

### Clinical Considerations
- **External Validation Required**: Performance on other populations unknown
- **Medical Supervision**: Requires clinical oversight for deployment
- **False Negative Risk**: 18.52% missed diagnosis rate requires careful evaluation
- **Regulatory Compliance**: May require FDA approval for clinical use

## 🔮 Future Development

### Immediate Roadmap
- [ ] **Multi-Population Validation**: Test on diverse demographic groups
- [ ] **Real-time Integration**: Connect with wearable devices and health trackers
- [ ] **Interactive Dashboard**: Web-based risk assessment interface
- [ ] **Mobile Application**: Point-of-care risk evaluation tool

### Technical Enhancements
- [ ] **Deep Learning**: Neural network ensemble integration
- [ ] **AutoML**: Automated model selection and optimization
- [ ] **Explainable AI**: Advanced interpretability methods
- [ ] **Edge Deployment**: Optimized models for mobile and IoT devices

## 🤝 Contributing

Contributions are welcomed for details on:

- Code style and standards
- Testing requirements
- Pull request process
- Issue reporting guidelines

### Development Setup
```bash
# Fork the repository and clone your fork
git clone https://github.com/ArthurTechy/AI-Based-Diabetes-Risk-prediction.git

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install development dependencies
pip install -r requirements-dev.txt

```

## 📊 Performance Benchmarks

### Comparison with Literature
| Method | Accuracy | Sensitivity | Specificity | AUC-ROC |
|--------|----------|-------------|-------------|---------|
| **Our Ensemble** | **74.68%** | **81.48%** | **71.00%** | **81.28%** |
| Traditional ML | 65-75% | 60-80% | 70-85% | 70-80% |
| Clinical Scoring | 60-70% | 50-70% | 75-90% | 65-75% |


## 📚 References & Citations

### Key Publications
1. Kaggle Dataset: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database
2. Original Research: Smith, J.W., Everhart, J.E., Dickson, W.C., Knowler, W.C., & Johannes, R.S. (1988). Using the ADAP learning algorithm to forecast the onset of diabetes mellitus. In Proceedings of the Symposium on Computer Applications and Medical Care (pp. 261-265).
3. Knowler, W.C., et al. (1990). "Diabetes incidence in Pima Indians: contributions of obesity and parental diabetes." American Journal of Epidemiology, 132(5), 902-909. 
4. Azur, M.J., et al. (2011). "Multiple imputation by chained equations: what is it and how does it work?" International Journal of Methods in Psychiatric Research, 20(1), 40-49. https://doi.org/10.1002/mpr.329


### Dataset Citation
```bibtex
@misc{pima_diabetes_dataset,
  title={Pima Indians Diabetes Database},
  author={National Institute of Diabetes and Digestive and Kidney Diseases},
  year={1990},
  publisher={UCI Machine Learning Repository}
}
```

## 📧 Contact & Support

- **Project Maintainer**: [Chiezie Arthur Ezenwaegbu](mailto:chiezie.arthur@gmail.com)
- **Issues**: [GitHub Issues](https://github.com/ArthurTechy/AI-Based-Diabetes-Risk-prediction/issues)

## 📄 License

This project is licensed under the MIT License 

### Disclaimer
The Interactive prediction for new data is intended for research and educational purposes. It is not intended to replace professional medical advice, diagnosis, or treatment. Always seek the advice of qualified healthcare providers with questions regarding medical conditions.

---
