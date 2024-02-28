# customer_segmentation_on_online_retail_data


# Customer Segmentation using K-Means Clustering

This project aims to segment customers based on their purchasing behavior using K-Means clustering. The dataset used in this project contains information about customer transactions, including their purchases, quantities, and invoice details.

## Dataset

The dataset (`online_retail.xlsx`) contains information about online retail transactions, including the following columns:

- `InvoiceNo`: Invoice number
- `StockCode`: Stock code of the purchased item
- `Description`: Description of the item
- `Quantity`: Quantity of the purchased item
- `InvoiceDate`: Date and time of the invoice
- `UnitPrice`: Price per unit of the item
- `CustomerID`: Unique identifier for the customer
- `Country`: Country where the transaction took place

The original Excel file (`online_retail.xlsx`) has been converted into a CSV file (`online_retail.csv`) for ease of use.


## Explanation of Code

1. **Data Preprocessing**:
   - The data is loaded from the CSV file (`customer_data.csv`).
   - Missing values in the 'CustomerID' column are dropped since customer segmentation is the focus.
   - Total spending is calculated by multiplying the 'Quantity' and 'UnitPrice' columns.
   - Frequency of purchases is calculated based on the number of unique dates of purchases per customer.

2. **Feature Selection**:
   - The relevant features for segmentation are selected, including 'Quantity', 'Total_Spending', and 'Frequency_of_Purchases'.

3. **Feature Scaling**:
   - Standard scaling is applied to normalize the features.

4. **K-Means Clustering**:
   - The optimal number of clusters is determined using the elbow method.
   - K-Means clustering is applied to segment customers into clusters based on their features.

5. **Visualization**:
   - Various visualizations are provided to explore the data and clustering results:
     - Histograms and boxplots of each selected feature.
     - Pairplot for pairwise feature relationships.
     - Scatter plot of clustered data points using PCA.

6. **Analysis**:
   - Cluster means are calculated to understand the characteristics of each cluster.

## Requirements

- Python 3.x
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

