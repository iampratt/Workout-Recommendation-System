# Workout Recommendation System

This repository contains a robust, data-driven system for recommending personalized workout routines using Python and Jupyter Notebook. The project is designed to suggest the best exercises for a user based on their fitness level, target muscle groups, and other personal fitness attributes.

---

## 🚀 Project Overview

**Goal:**  
Recommend the best workouts for each user based on:
- Fitness experience level
- Target muscle group
- Personal fitness goals
- Workout difficulty
- Body part focus
- Workout frequency
- Estimated calories burned

**Input Features:**
- Experience Level (Beginner / Intermediate / Advanced)
- Target Muscle Group (Chest, Legs, Back, Core, Full Body, etc.)
- Difficulty Level (Easy, Medium, Hard)
- Body Part (Upper, Lower, Core, Full)
- Workout Frequency (days/week)
- Estimated Calories Burned per session

**Output:**  
A personalized list of workouts, including:
- Name of Exercise
- Target Muscle Group
- Difficulty Level
- Calories Burned (per session)
- (And optionally, equipment and benefits)

---

## 🏗️ How It Works

- **Data Cleaning:**  
  The notebook includes extensive cleaning and normalization of exercise names, target muscle groups, and difficulty levels to ensure consistent recommendations.

- **Feature Engineering:**  
  Combines exercise metadata (like target muscle, difficulty, calories) to create a comprehensive feature set for similarity-based recommendations.

- **Recommendation Logic:**  
  - Uses text similarity (TF-IDF + cosine similarity) to recommend exercises similar to a user's input.
  - Provides filters for user-specific needs (e.g., muscle group, difficulty).
  - Includes a fallback system for fuzzy matching and offers randomized suggestions when exact matches are lacking.
  - Supports variety in recommendations by calorie intensity (light, medium, intense).

- **Model Export:**  
  The notebook provides functionality to export a trained recommender as a pickle file for deployment or further use.

---

## 📁 Repository Structure

- `workout_recommendation_system.ipynb` — Main notebook with all data processing, exploration, model building, and recommendation code.
- `README.md` — This file.
- `fitness_recommender.pkl` — (Optional) Serialized recommender object for deployment.
- `Final_data.csv` — The dataset used (not included in the repo, add your own).

---

## ⚡ Getting Started

### Prerequisites

- Python 3.7+
- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `wordcloud`
- `fuzzywuzzy` for fuzzy matching
- `jupyter` for running the notebook

Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn wordcloud fuzzywuzzy
```

### Running the Notebook

1. Clone the repository:
    ```bash
    git clone https://github.com/iampratt/Workout-Recommendation-System.git
    cd Workout-Recommendation-System
    ```

2. Ensure your data file (e.g., `Final_data.csv`) is present in the working directory.

3. Launch Jupyter Notebook and open `workout_recommendation_system.ipynb`:
    ```bash
    jupyter notebook
    ```

4. Run the notebook cells step-by-step to process data, build the recommender, and generate workout suggestions.

---

## 📝 Example Usage

- **Get similar exercises to "Push Ups" for an Intermediate level:**  
  Use the `recommend_intermediate("Chest")` function (or use the GUI/interactive cells in the notebook).

- **Save your own recommender:**  
  The notebook shows how to create and pickle a `FitnessRecommender` object for later use.

---

## ⚙️ Customization

- Add or modify the dataset in `Final_data.csv` to include more exercises, custom fields, or user-specific data.
- Adjust recommendation filters or logic in the notebook to suit your needs.
- Integrate with a web app or API by loading the exported `.pkl` model.

---

## 🤝 Contributing

Pull requests, suggestions, and issues are welcome! If you have ideas for improvement or want to add new features, feel free to contribute.

---

## 👤 Author

Pratyush Srivastava  
RS Project | 229302071

---

**Explore, adapt, and build your own smart fitness recommendation system!**
