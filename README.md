# Startup Success Predictor

Predicts whether a startup will succeed or fail using machine learning.

## Overview
Startups drive innovation but **~90% fail in the first few years**. This project uses historical data to predict startup outcomes, helping entrepreneurs, investors and accelerators make informed decisions.

## Features
- Supervised ML models:
  - K-Nearest Neighbors (KNN)
  - Logistic Regression
  - Naive Bayes
  - Decision Tree
- Evaluates model performance
- Provides insights on key success factors

## Target Users
- Entrepreneurs
- Investors
- Incubators and Accelerators

## Tech Stack

### Core Technologies
- **Python 3** - Primary programming language
- **Jupyter Notebook** - Interactive analysis and documentation
- **Google Colab** - Cloud-based notebook environment

### Data Science Libraries
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib/Seaborn** - Data visualization

### ML Algorithms
- **K-Nearest Neighbors (KNN)** - Non-parametric classification
- **Logistic Regression** - Linear classification
- **Naive Bayes** - Probabilistic classifier
- **Decision Tree** - Tree-based classification

## Dataset

### Data Source
- **File**: `startup_dataset.csv`
- **Size**: ~11 MB
- **Records**: 66,368 startups
- **Features**: 14 columns

### Key Features

| Column | Type | Description |
|--------|------|-------------|
| `permalink` | String | Unique company identifier path |
| `name` | String | Company name |
| `homepage_url` | String | Company website URL |
| `category_list` | String | Business categories (pipe-separated) |
| `funding_total_usd` | Float | Total funding received in USD |
| `status` | String | Current status (operating, acquired, closed) |
| `country_code` | String | ISO country code |
| `state_code` | String | State/province code |
| `region` | String | Geographic region |
| `city` | String | City location |
| `funding_rounds` | Integer | Number of funding rounds |
| `founded_at` | Date | Company founding date |
| `first_funding_at` | Date | Date of first funding |
| `last_funding_at` | Date | Date of most recent funding |

### Data Characteristics
- **Target Variable**: `status` (operating = success, closed = failure, acquired = varies)
- **Missing Values**: Present in geographic and categorical fields
- **Data Type Issues**: Funding amounts stored as strings (require conversion)
- **Geographic Coverage**: Global dataset spanning multiple countries and regions
- **Time Range**: Startups founded from early 2000s through 2015

## Getting Started

### Prerequisites
- Python 3.6+
- Jupyter Notebook or Google Colab account
- pip (Python package manager)

### Installation

#### Local Setup
```bash
# Clone the repository
git clone https://github.com/ghaidabs/Startup-Success-Prediction.git
cd Startup-Success-Prediction

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

#### Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Click "File" → "Open notebook"
3. Go to "GitHub" tab
4. Enter: `ghaidabs/Startup-Success-Prediction`
5. Open `main.ipynb`

### Running the Analysis

#### Local Jupyter
```bash
jupyter notebook main.ipynb
```

#### Google Colab
- Open the notebook directly in Colab
- Run cells sequentially with Shift+Enter
- Upload `startup_dataset.csv` if needed


## Challenges & Considerations

### Data Quality Issues
- **Missing Values**: Geographic fields have significant missing data
- **Data Type Issues**: Funding stored as strings (requires parsing)
- **Date Inconsistencies**: Some founding dates appear invalid (e.g., year 1015)
- **Unknown Status**: Some startups have ambiguous status values

### Modeling Challenges
- **Class Imbalance**: May have uneven success/failure distribution
- **Feature Engineering**: Requires domain expertise to create meaningful features
- **Temporal Aspects**: Startup success changes over time
- **Definition Ambiguity**: "Success" can mean operating, acquired, or profitable

### Best Practices Applied
- Handle missing data appropriately
- Validate data before modeling
- Use cross-validation for robust evaluation
- Compare multiple algorithms
- Interpret results cautiously

## Results & Findings

The notebook demonstrates:
- ✅ Data loading and preprocessing workflow
- ✅ Exploratory analysis of startup patterns
- ✅ Feature extraction from raw data
- ✅ Training multiple classification models
- ✅ Evaluating and comparing model performance
- ✅ Extracting actionable business insights
