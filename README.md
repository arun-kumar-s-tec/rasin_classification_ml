# 🍇 Raisin Class Predictor

An interactive Streamlit web application that classifies raisin varieties into **Kecimen** or **Besni** based on their physical and geometrical features. The underlying machine learning model is built using an optimized `RandomForestClassifier` trained on the Raisin Dataset.

---

## 🚀 Live Demo
*(Optional: If you host it on Streamlit Community Cloud, place your deployment link here)*
👉 [Live Web App Link](https://rasinclassificationmldemo.streamlit.app/)

---

## 📊 Features
* **Automated Model Training:** The application automatically loads the dataset and trains a Random Forest model on launch (efficiently cached for speed).
* **Interactive Controls:** Sidebars with numeric inputs and sliders allow you to tweak the raisin's physical metrics.
* **Real-time Inference:** Instantly predicts the raisin variety as soon as you press the **Predict Class** button.
* **Confidence Metrics:** Provides a dynamic probability bar chart visualizing the model's prediction confidence for both classes.

---

## 🛠️ Dataset Overview
The app utilizes 7 key morphologic features extracted via image processing to differentiate between the varieties:
1. **Area:** The number of pixels within the boundaries of the raisin.
2. **MajorAxisLength:** The distance between the ends of the longest line that can be drawn on the raisin.
3. **MinorAxisLength:** The distance between the ends of the shortest line that can be drawn on the raisin.
4. **Eccentricity:** Eccentricity of the ellipse, measuring how elongated the shape is.
5. **ConvexArea:** The number of pixels in the smallest convex polygon that can contain the region.
6. **Extent:** The ratio of the region area to the bounding box area.
7. **Perimeter:** The total distance around the boundary of the raisin.

---

## 🤖 Model Specifications
The machine learning pipeline is configured using parameters fine-tuned in the development notebook:
* **Algorithm:** Random Forest Classifier (`sklearn.ensemble.RandomForestClassifier`)
* **Estimators ($n$):** 10 trees
* **Criterion:** Gini impurity
* **Max Depth:** 100
* **Data Split:** 90% Training, 10% Testing

---
