# NBA Stats Predictor

A deep learning tool that predicts NBA player statistics using historical data. The model analyzes player career trajectories to forecast future performance on a season-by-season basis.

## 🏀 Features

- **Data Collection**: Automated scraping of NBA player statistics directly from the NBA
- **Data Processing**: Comprehensive preprocessing including normalization and variable-length sequence preparation
- **Model Training**: LSTM-based deep learning model for time-series prediction
- **Statistics Prediction**: Forecasts key player statistics for upcoming seasons
- **Model Persistence**: Save and load trained models for future use

## Project Structure

```
nba-stats-predictor/
├── data/                           # Generated data files
│   ├── nba_player_stats_*.csv     # Historical player statistics
│   ├── predicted_*_season.csv     # Model predictions
│   └── ...                        
├── scraper.ipynb                  # Web scraping notebook
├── trainer.ipynb                  # Model training notebook
├── guesser.ipynb                  # Prediction interface
├── nba_stats_predictor_model.keras # Saved model (generated)
└── normalization_params.json      # Model parameters (generated)
```

## How It Works

1. **Data Collection** (`scraper.ipynb`):
   - Scrapes historical NBA player statistics
   - Processes and cleans the raw data
   - Saves data to CSV format

2. **Model Training** (`trainer.ipynb`):
   - Preprocesses data for deep learning
   - Saves preprocessed data to CSV format
   - Implements and trains LSTM model
   - Saves trained model and normalization parameters

3. **Predictions** (`guesser.ipynb`):
   - Loads trained model and parameters
   - Makes predictions for future seasons
   - Exports predictions to CSV files

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/srhn45/nba-stats-predictor.git
cd nba-stats-predictor
```

2. Install required packages:
```bash
pip install tensorflow pandas numpy sklearn
```

3. Run notebooks in order:
   - First run `scraper.ipynb` to collect data
   - Then `trainer.ipynb` to train the model
   - Finally `guesser.ipynb` to make predictions
  
   - Can run `guesser.ipynb` directly with the provided data if not looking to make changes

## Generated Files

The following files are generated through the notebooks:

- `data/nba_player_stats_*.csv`: Contains scraped NBA statistics
- `data/predicted_*_season.csv`: Contains model predictions
- `nba_stats_predictor_model.keras`: Trained model file
- `normalization_params.json`: Model normalization parameters

Note: All generated files can be recreated by running the notebooks in sequence.

## Future Improvements and Additions

- Add player similarity analysis
- Implement confidence intervals for predictions
- Add injury history consideration
- Expand to team-level predictions
  
- Develop Fantasy Draft AI Bot using predictions
  - Implement reinforcement learning for optimal draft strategies
  - Consider league-specific scoring systems
  - Account for position scarcity and roster construction
  - Optimize for season-long performance using predicted statistics
  - Adapt strategy based on draft position

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
