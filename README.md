# Player-Song-Recommender-System
**🎵 MLB Walk-Up Music Impact Analysis & Song Recommendation System
📌 Project Overview**

This project investigates whether a baseball player's walk-up song influences their home-game performance—specifically their Home OPS (On-base Plus Slugging).
By combining MLB player stats (2022–2025), Spotify song audio features, and biographical player data, a machine learning model was built to estimate how musical characteristics (energy, valence, tempo, danceability, etc.) affect performance.
Finally, the model recommends personalized walk-up songs that could potentially improve each player’s predicted OPS.




**🎯 Key Objectives**

Analyze whether music influences player performance.
Build a predictive model for Home OPS using:
Player skill indicators
Biographical attributes
Song audio features
Simulate replacing walk-up songs and identify the most performance-boosting tracks.




**📂 Dataset Components**

Merged into merged_cleaned_dataset.csv:
MLB home & away performance metrics
Walk-up song list
Spotify song features (13 attributes)
Player biographical data (age, handedness, experience)
Data cleaning included missing-value handling, date standardization, and merging multi-source records.




**🛠️ Feature Engineering**

Key engineered variables:

HOME_OPS → Target variable
AWAY_OPS → Control variable for overall ability
AGE → Derived from birth year
PLAYER_FREQ → Player experience
Song Features → 13 numerical audio descriptors




**🤖 Modeling Approach**

A Random Forest Regressor was selected due to:
Ability to handle non-linear relationships
Robustness to overfitting
Support for mixed numerical features




Model Performance
Metric	Score
R²	0.894
RMSE	0.084

This means the model explains ~90% of variation in Home OPS and makes highly accurate predictions.




**🎶 Insights**

What musical attributes correlate with higher performance?
High Energy
Positive Mood (Valence)
High Danceability

Players tend to perform better when walking up to upbeat, motivational, rhythmic songs.




**🎧 Song Recommendation Simulation**

For each of the nine target players:
Their current walk-up song was replaced with 150 popular tracks
The model predicted the new Home OPS
The best-performing song was selected for each player

Example:
A player received the song “Spooky” – Dusty Springfield, resulting in +0.00022 predicted OPS improvement due to its steady, calm rhythm.




Average predicted improvements ranged from +0.02 to +0.06 OPS—small but consistent.




**🧠 Workflow**

From page 5 diagram:

Data Collection

Data Cleaning & Merging
Feature Engineering
Model Training (Random Forest)
Song Simulation
Recommendation Output




**📌 Reflection & Next Steps**

Future improvements may include:

Incorporating pitcher quality & park effects
Adding batter–pitcher matchup data
Running real-world A/B experiments
Expanding to other performance metrics (WAR, slugging %, etc.)
