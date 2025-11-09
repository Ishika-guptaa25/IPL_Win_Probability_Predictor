<h1 align="center">🏏 IPL Win Probability Predictor</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
</p>

---

## 🎯 Overview  

**IPL Win Probability Predictor** is a machine learning-powered web app built using **Python** and **Streamlit**.  
It predicts the **winning probability** of IPL teams during a live or simulated match based on inputs like runs, overs, wickets, and target.  

> ⚡ *Real-time insights for cricket lovers and analysts — powered by data and machine learning!*  

---

## 📌 Features  

✅ Select **Batting** and **Bowling** teams from all IPL franchises  
✅ Choose the **Host City**  
✅ Input live match data — **Target, Score, Overs, and Wickets**  
✅ Get **real-time Win/Loss probabilities** instantly  
✅ Built with a **Fast, Interactive Streamlit UI**  

---

## 🗂️ Project Structure  

<img width="824" height="238" alt="image" src="https://github.com/user-attachments/assets/b063dda6-286c-464d-9b28-794261463860" />


---

## ⚙️ How It Works  

### 🧩 Input  
- Batting team  
- Bowling team  
- Host city  
- Target score  
- Current score  
- Overs completed  
- Wickets fallen  

### 🧮 Behind the Scenes  

```python
runs_left = target - current_score
balls_left = 120 - (overs * 6)
wickets_remaining = 10 - wickets
CRR = current_score / overs
RRR = (runs_left * 6) / balls_left

**Prediction**:
   - A `RandomForestClassifier` or similar model (loaded via `pipe.pkl`) predicts win probability for the batting team.
```
##  Getting Started
```
### 1.Install Dependencies
```bash
pip install streamlit pandas scikit-learn
```
### 2. Add Model File
```bash
Ensure that pipe.pkl (your trained model pipeline) is placed in the root directory.
```
### 3. Run the App
```bash
streamlit run app.py
```

<p align="center"> <img width="948" height="798" alt="image" src="https://github.com/user-attachments/assets/3c66ecd6-7b46-40a3-af75-c2c0bfc2dcd9" /> </p>
This screenshot shows the Streamlit web app interface predicting the win probability between two IPL teams in real time.

