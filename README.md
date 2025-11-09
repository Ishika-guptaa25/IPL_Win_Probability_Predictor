🏏 IPL Win Probability Predictor
This is a machine learning-based IPL Win Probability Predictor built using Python and Streamlit. Given the match conditions like batting team, bowling team, score, overs, and wickets, the model predicts the probability of the batting team winning the match.

📌 Features
🏏 Select batting and bowling teams from all IPL franchises
🏟️ Choose the host city
🔢 Enter match statistics (target, score, overs, wickets)
📊 Get real-time win/loss probability using a trained machine learning model
⚡ Fast and interactive UI with Streamlit
🗂️ Project Structure
Image

⚙️ How It Works
Input:

Batting team
Bowling team
Host city
Target score
Current score
Overs completed
Wickets fallen
Calculation:

runs_left = target - current_score
balls_left = 120 - overs * 6
wickets_remaining = 10 - wickets
CRR = current_score / overs
RRR = (runs_left * 6) / balls_left
Prediction:

A RandomForestClassifier or similar model (loaded via pipe.pkl) predicts win probability for the batting team.
🚀 Getting Started
1. Clone the Repository
git clone https://github.com/yourusername/ipl-win-predictor.git
cd ipl-win-predictor
2.Install Dependencies
pip install streamlit pandas scikit-learn
###3. Add Model File

Ensure that pipe.pkl (your trained model pipeline) is placed in the root directory.
4. Run the App
streamlit run app.py
📷 Sample Screenshot Image

📄 Model Training (Optional)
*The model is trained separately using IPL ball-by-ball and match-level data. Feature engineering includes:

*Calculating match context (runs left, balls left, etc.)

*Encoding teams and cities

*Training a classifier with historical outcomes

**Note: The training process is documented in the notebook IPL_Win_Probability_Predictor.ipynb.
