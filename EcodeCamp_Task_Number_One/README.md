# **Customer Churn Analysis**

## **Table of Contents**
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## **Introduction**
This project performs an exploratory data analysis (EDA) on the Telco Customer Churn dataset to identify factors that influence customer churn. The dataset includes customer demographics, account information, and subscription details. The goal is to gain insights into customer behavior, highlight key factors that drive churn, and suggest potential strategies for customer retention.

## **Dataset**
The dataset used in this project is the **Telco Customer Churn** dataset, which can be found on [Kaggle](https://www.kaggle.com/blastchar/telco-customer-churn). The dataset includes customer information and a `Churn` column indicating whether a customer left the company or not.

### **Features**
- **Target Variable:**
  - `Churn`: Whether the customer has churned (Yes/No).
  
- **Key Features:**
  - `tenure`: Duration of the customer’s stay.
  - `MonthlyCharges`: The monthly amount billed to the customer.
  - `TotalCharges`: The total amount billed over time.
  - `Contract`, `PaymentMethod`, `InternetService`: Categorical variables representing subscription details.

## **Installation**
To run this project locally, you will need to have Python installed. Follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/customer-churn-analysis.git
    cd customer-churn-analysis
    ```

2. Install the necessary dependencies by running the following command:
    ```bash
    pip install -r requirements.txt
    ```

### **Dependencies:**
- pandas
- numpy
- seaborn
- matplotlib
- plotly
- scikit-learn
- xgboost

These can be installed via the `requirements.txt` file.

## **Project Structure**
The project is structured as follows:

```bash
customer-churn-analysis/
│
├── data/
│   └── telco_customer_churn.csv  # The dataset (add your data here)
│
├── notebooks/
│   ├── EDA.ipynb                 # Jupyter notebook for data analysis
│   ├── churn_prediction.ipynb     # Jupyter notebook for model training
│
├── visuals/
│   ├── correlation_matrix.png     # Correlation matrix visualization
│   ├── churn_distribution.png     # Churn distribution visualization
│   ├── ...                        # Other visualizations
│
├── README.md                      # Project README file
├── requirements.txt               # Python dependencies
├── main.py                        # Main analysis script
└── LICENSE                        # License file
```

## **Exploratory Data Analysis**
The analysis covers:
- Handling missing values (filling `TotalCharges`).
- Encoding categorical variables.
- Normalization of numerical columns.
- Visualizing data distribution using histograms, correlation heatmaps, and churn distribution plots.

### **Key Visualizations**
- **Correlation Matrix**: Shows correlations between numerical features (`tenure`, `MonthlyCharges`, etc.) and `Churn`.
- **Churn Distribution**: Proportion of churned vs. non-churned customers.
- **Histograms**: Display the distribution of key features like `tenure`, `MonthlyCharges`, and `TotalCharges`.
- **Violin Plot**: Senior citizen distribution by churn.
- **Contract Type and Churn**: Visualizes the relationship between customer contract types and churn.

You can find these visualizations in the `visuals/` folder.

## **Conclusion**
Based on the analysis, it was found that:
- Customers with high `MonthlyCharges` and short `tenure` tend to churn more.
- Customers with month-to-month contracts have higher churn rates compared to customers with yearly contracts.
- Important features for predicting churn include `MonthlyCharges`, `tenure`, and `Contract`.

**Business Recommendation:**  
To reduce churn, it is suggested to:
- Focus on customers with month-to-month contracts and provide incentives for long-term contracts.
- Offer promotions to customers who are in the early months of service and have high `MonthlyCharges`.

## **Usage**
1. You can open and run the notebooks located in the `notebooks/` directory to walk through the exploratory data analysis and machine learning model training.
2. Run the `main.py` file to execute the analysis and churn prediction in a single script.
    ```bash
    python main.py
    ```

3. After running the code, visualizations will be saved in the `visuals/` directory, and you can view them to interpret the analysis.

## **Contributing**
Feel free to submit issues or fork the repository and submit pull requests. Contributions are welcome! Please make sure your contributions follow the project guidelines.

## **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

