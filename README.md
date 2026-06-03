# Used Car Price Prediction 🚗💰

## 📌 Project Overview
This project applies Supervised Machine Learning to predict the selling price of used cars based on various historical and technical features. By analyzing the dataset, the project walks through a complete end-to-end Machine Learning lifecycle, including data preprocessing, extensive model comparison, hyperparameter tuning, and evaluation.

## 📊 Dataset Information
The primary data source is `cardekho_imputated.csv`. This dataset contains pre-cleaned and imputed vehicle records, including features such as:
* Vehicle Age / Year of Manufacture
* Mileage and Engine Specifications
* Fuel Type and Transmission Type
* **Target Variable:** Selling Price

## 🛠️ Project Lifecycle & Workflow
1. **Data Preprocessing:** Utilized Scikit-Learn's `ColumnTransformer` to create a robust pipeline.
    * Applied `StandardScaler` to numerical features to optimize distance-based model performance.
    * Applied `OneHotEncoder` to convert categorical text data into a machine-readable binary format.
2. **Extensive Model Training:** Built and evaluated a wide array of regression algorithms to find the optimal fit for non-linear vehicle depreciation:
    * Linear Regression
    * Ridge Regression
    * Lasso Regression
    * Elastic Net Regressor
    * Decision Tree Regressor
    * Random Forest Regressor
    * K-Neighbors Regressor
3. **Hyperparameter Tuning:** Implemented `RandomizedSearchCV` with cross-validation to find the optimal parameters for the top-performing models.
4. **Model Evaluation:** Assessed training and testing performance using Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R² Score.

## 🏆 Model Performance & Conclusion
After extensive testing across linear, distance-based, and tree-based algorithms, the **Random Forest Regressor** and **K-Neighbors Regressor (KNN)** heavily outperformed the others. 

The linear models (Linear, Ridge, Lasso, Elastic Net) struggled to capture the complex, non-linear nature of car depreciation and categorical price jumps. Random Forest and KNN successfully mapped these complex relationships, yielding the highest R² scores and lowest error metrics.

## 🗂️ Repository Structure
* `used_car.ipynb`: The primary Jupyter Notebook containing the full workflow, from data ingestion to model comparison and evaluation.
* `cardekho_imputated.csv`: The dataset used for training and testing the models.

## 💻 Technologies & Libraries Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Environment:** Jupyter / VS Code / Conda
