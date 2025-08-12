# purrceptron.py
# Simple Cat vs Dog classifier using height, weight, length

import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.neural_network import MLPClassifier
from sklearn.metrics import accuracy_score

# --- 1. Simulated dataset ---
# Features: [height_cm, weight_kg, length_cm]
# Label: 0 = cat, 1 = dog
X = np.array([
    [25, 4, 40],  # Cat
    [23, 3.5, 38],# Cat
    [30, 5, 45],  # Cat
    [55, 20, 90], # Dog
    [60, 22, 95], # Dog
    [50, 18, 85], # Dog
    [28, 4.2, 42],# Cat
    [58, 21, 88], # Dog
    [26, 3.8, 39],# Cat
    [52, 19, 87]  # Dog
])
y = np.array([0,0,0,1,1,1,0,1,0,1])

# --- 2. Split into train/test ---
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# --- 3. Build Neural Network ---
model = MLPClassifier(
    hidden_layer_sizes=(4,),  # 1 hidden layer with 4 nodes
    activation='logistic',    # sigmoid activation
    max_iter=1000,
    random_state=42
)

# --- 4. Train ---
model.fit(X_train, y_train)

# --- 5. Predict ---
y_pred = model.predict(X_test)
y_prob = model.predict_proba(X_test)[:, 1]  # Probability of being dog

# --- 6. Evaluate ---
print("Test Accuracy:", accuracy_score(y_test, y_pred))
for features, pred, prob in zip(X_test, y_pred, y_prob):
    species = "Dog" if pred == 1 else "Cat"
    print(f"Input {features} => {species} (P(dog) = {prob:.2f})")
