🔋 Energy Consumption Audit Using Decision Tree
This project audits and classifies the energy consumption efficiency of countries using a Decision Tree Classifier, based on their GDP and energy consumption per capita. The analysis is based on 2020 data from the OWID Energy Dataset.

<br>
📌 Project Objective
To demonstrate how a simple machine learning model can:

Classify countries into Efficient, Moderate, or Inefficient based on energy usage and GDP.

Help uncover insights into global energy efficiency patterns.

Highlight countries that can serve as benchmarks for sustainable development.

<br>
📂 Dataset
Source: OWID Energy Dataset

File used: owid-energy-data.csv

Filtered for the year 2020

Key features:

gdp (GDP per capita)

energy_per_capita (Energy consumption per capita)

<br>
🧪 Steps Performed
🔰 1. Import Libraries
Used pandas, numpy, matplotlib, seaborn, and scikit-learn (sklearn).

🟠 2. Load Dataset
Read owid-energy-data.csv and explored the initial rows.

🟡 3. Preprocessing
Dropped rows with missing gdp or energy_per_capita.

Filtered data to only include entries from 2020.

🟢 4. Labeling
Created a new column efficiency_class:

Efficient: High GDP (≥ 20,000) & low energy use (≤ 3,000 kWh)

Moderate: Everything else

Inefficient: Low GDP (< 10,000) & high energy use (> 5,000 kWh)

⚠️ In 2020 data, no countries met the criteria for Inefficient.

🟠 5. Feature Selection
Features: gdp, energy_per_capita

Target: efficiency_class

🟡 6. Modeling
Split dataset into train/test (80:20)

Trained using DecisionTreeClassifier

Achieved 100% accuracy on the test set (due to limited class diversity)

🟢 7. Visualization
Scatter Plot of countries based on GDP vs energy usage

Decision Tree structure visualization

Confusion Matrix

Distribution bar chart by efficiency class

Prediction result table with country names

<br>
🎯 Key Findings
Most countries fall in the Moderate category.

Only ~40 countries were classified as Efficient.

No country in 2020 met the threshold to be considered Inefficient.

The model performed perfectly within this data subset but is likely overfitting due to class imbalance.

There is a significant opportunity for many countries to improve energy efficiency.

<br>
📈 Visual Examples
<details> <summary>📊 Click to expand some key visuals</summary>
Scatter plot (GDP vs Energy Use)

Decision Tree structure

Confusion matrix

Country classification distribution


##⚙️ How to Run

1. Clone this repository:
git clone https://github.com/yourusername/energy-audit-decision-tree.git
cd energy-audit-decision-tree

2. Install dependencies:
pip install pandas numpy matplotlib seaborn scikit-learn

3. Run the notebook or script:
python energy_audit_decision_tree.py
📄 Note: Make sure owid-energy-data.csv is in the same folder as the script.

##✅ Dependencies
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn


##🧠 Future Improvements
- Include data from multiple years (not just 2020).
- Handle class imbalance by synthetic data generation or resampling.
- Add more features like CO₂ emissions, renewable energy usage, etc.
- Try other models (Random Forest, Gradient Boosting, etc.)

##🤝 Contributions
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

##🌍 Author
Qonita Qotrunnada
Data Science, Front-end, & IoT Enthusiast
📧 [YourEmail@example.com]
🔗 LinkedIn • GitHub
