# NFL Win Probability Analysis

This project analyzes NFL game data to identify and visualize "blown" games where teams lost despite having a high win probability late in the game.

## Overview

The analysis focuses on identifying games where teams had a win probability greater than 70% in the fourth quarter (last 10 minutes) but ultimately lost the game. It includes specific analysis for all NFL teams and detailed visualization of the Baltimore Ravens' blown games.

## Data Requirements

The project requires two CSV files:
- `pbp_stats.csv`: Play-by-play statistics including:
  - game_id
  - qtr (quarter)
  - game_seconds_remaining
  - home_wp (home team win probability)
  - away_wp (away team win probability)
  - home_team
  - away_team
  - home_score
  - away_score
  - posteam (team with possession)
  - defteam (defensive team)

- `players.csv`: Player information (referenced in the code but not currently used in analysis)

## Key Features

1. **League-wide Analysis**
   - Identifies blown games across all NFL teams
   - Calculates and ranks teams by number of blown games
   - Generates visualizations using seaborn for team comparisons

2. **Ravens-specific Analysis**
   - Detailed analysis of Baltimore Ravens' blown games
   - Tracks games where Ravens had >70% win probability but lost
   - Generates win probability charts for each blown game

## Parameters

- WIN_PROB_THRESHOLD = 0.70 (70% win probability)
- TIME_THRESHOLD = 600 (last 10 minutes of the game)

## Output Files

The script generates several outputs:
- `ravens_blown_games.csv`: Detailed information about Ravens' blown games
- Win probability charts for each blown game (saved as PNG files)
- Console output showing blown games statistics

## Visualization

The project creates two types of visualizations:
1. Bar chart showing the number of blown games by team
2. Individual game win probability charts showing:
   - Home team win probability (purple line)
   - Away team win probability (black line)
   - 4th quarter marker (red dashed line)

## Dependencies

- pandas
- matplotlib
- seaborn
- google.colab (if running in Google Colab environment)

## Usage

1. Ensure all required CSV files are in the correct directory
2. Run the script to generate:
   - League-wide analysis
   - Ravens-specific analysis
   - Visualizations

## Game ID Format

Game IDs follow the format: `YYYY_WW_HOME_AWAY` where:
- YYYY: Year
- WW: Week number (01-18)
- HOME: Home team abbreviation
- AWAY: Away team abbreviation

Example: '2021_01_BAL_LV' represents 2021 Week 1 game, Baltimore vs Las Vegas
