# Online Retail Transaction Analysis

## Project Overview
This project analyses transactional data from a UK-based online retailer 
covering the period 2010-2011. The goal is to uncover insights about 
customer behaviour, product popularity, sales trends, and pricing patterns 
to support data-driven business decisions.

## Target Audience
- E-commerce managers looking to understand customer behaviour
- Marketing teams seeking to optimise campaigns
- Product managers wanting to improve product strategy

## Business Requirements
1. Which products are sold the most by quantity?
2. How have sales developed month by month over the years?
3. Is there a correlation between product price and quantity sold?
4. How is UnitPrice distributed and can it be normalised?

## Project Hypothesis
1. A small number of products will account for the majority of total sales (Pareto principle)
2. Sales will peak in November-December due to Christmas shopping
3. Products with a lower unit price will have a higher quantity sold
4. UnitPrice will be right-skewed and can be normalised with Box-Cox transformation

## Dataset
- **Source:** [Online Retail Transactions Dataset](https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset) (Kaggle)
- **Records:** 524,878 transactions after cleaning
- **Period:** December 2010 – December 2011
- **Columns:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

## Project Structure
```
DA_project_1/
├── data/
│   ├── source/          # Raw dataset files
│   └── processed/       # Cleaned dataset
├── jupyter_notebooks/
│   ├── 01_load_and_clean_data.ipynb
│   ├── 02_analysis_and_visualizations.ipynb
│   └── 03_summary.ipynb
├── requirements.txt
└── README.md
```

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Run `01_load_and_clean_data.ipynb` to clean the data
3. Run `02_analysis_and_visualizations.ipynb` for analysis and visualisations
4. Run `03_summary.ipynb` for conclusions

## Hypothesis Validation
| Hypothesis | Result |
|------------|--------|
| A small number of products drive the majority of sales (Pareto) | Partially supported |
| Sales peak in November-December due to Christmas shopping | Supported |
| Lower-priced products sell in higher quantities | Supported |
| UnitPrice is right-skewed and normalisable with Box-Cox | Confirmed |

## Technologies Used
- **Python 3.12**
- **Pandas** — data manipulation
- **Matplotlib & Seaborn** — data visualisation
- **Plotly** — interactive visualisations
- **Feature Engine** — Box-Cox transformation
- **Scikit-learn** — pipeline
- **Pingouin** — statistical analysis
- **Jupyter Notebook** — development environment
- **GitHub** — version control

## Design Decisions
- Scatter plot was chosen over box plot for BR3 as it better shows 
  the relationship between two continuous variables
- Box-Cox was preferred over log transformation as it optimises 
  the lambda parameter automatically

## Challenges
- Interactive Plotly plots require nbformat>=4.2.0 which was not 
  available in the environment — resolved with browser fallback
- GitHub Copilot occasionally suggested overly complex solutions 
  that needed to be simplified for the scope of this project

## Credits

### Dataset
- [Online Retail Transactions Dataset](https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset) by Abhishek R P on Kaggle

### AI Assistance
- GitHub Copilot — used for code review, suggestions and summarisation
- The specific contributions of AI tools are documented in each notebook
- Claude (Anthropic) — used for guidance, problem-solving, and code review during development; also used post-completion for project maintenance (see summary notebook for details)

## Acknowledgements
- Code Institute LMS — course material and project template
- Marcel (mentor) — guidance throughout the project