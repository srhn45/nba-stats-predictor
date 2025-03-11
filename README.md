# NBA Stats Predictor

A sophisticated deep learning tool that predicts NBA player statistics by analyzing historical performance data. This project uses the NBA API to collect comprehensive player statistics and employs deep learning to forecast individual player performance for upcoming, current, or historical seasons.

## 🏀 Features

- **Comprehensive Data Collection**
  - Automated scraping of NBA player statistics using the official NBA API
  - Collection of per-game statistics including points, rebounds, assists, and more
  - Historical data dating back to 1980
  - Rate-limited API calls to ensure reliable data collection

- **Data Processing**
  - Conversion of season totals to per-game statistics
  - Intelligent handling of missing data
  - Advanced data normalization with masked value support
  - Career sequence creation for temporal analysis

- **Deep Learning Prediction Model**
  - Sequential player career analysis
  - Prediction of multiple statistical categories
  - Validation on out-of-sample data
  - Support for both current and historical season predictions
 
## 🚀 Upcoming

### Model Improvements
- Optimization of the base deep learning model
  - Fine-tuning of hyperparameters
  - Exploration of alternative architectures
  - Performance benchmarking against different approaches

### Pre-trained Model Inclusion
- Addition of pre-trained model files to the repository
- Easy-to-use model loading functionality
- Documentation for using pre-trained models
- Version tracking for different model iterations

### Data Updates
- Will try to keep the included data up to date

Stay tuned!

## 🛠️ Technology Stack

- **Python 3.x**
- **Key Libraries**:
  - `nba_api`: Official NBA stats API client
  - `pandas`: Data manipulation and analysis
  - `numpy`: Numerical computing
  - `tensorflow/keras`: Deep learning implementation
  - `jupyter`: Interactive development environment

## 📋 Prerequisites

1. Python 3.8 or higher
2. Jupyter Notebook
3. pip (Python package manager)

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/srhn45/nba-stats-predictor.git
cd nba-stats-predictor
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## 💻 Usage

The project consists of two main Jupyter notebooks:

1. **scraper.ipynb**
   - Collects historical NBA player statistics
   - Features automatic rate limiting and error handling
   - Saves data in CSV format for further processing

2. **guesser.ipynb**
   - Processes and normalizes the collected data
   - Implements the prediction model
   - Provides player performance forecasting

To run the project:

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. First run `scraper.ipynb` to collect the data
3. Then run `guesser.ipynb` to train the model and make predictions

## 📊 Data Collection

The `NBADataCollector` class handles data collection with the following features:

- Automatic rate limiting to prevent API timeouts
- Incremental progress saving
- Error logging and recovery
- Per-game statistics calculation
- Season identification and filtering

## 🤖 Model Architecture

The prediction model:
- Uses sequential career data to predict future performance
- Implements masked value handling for incomplete seasons
- Splits data into training and validation sets (90/10 split)
- Normalizes statistics while preserving data integrity

## 📈 Performance Metrics

The model evaluates predictions using:
- Per-game statistics accuracy
- Player career trajectory analysis
- Out-of-sample validation
- Historical season comparisons
