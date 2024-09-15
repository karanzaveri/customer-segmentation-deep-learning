
# Customer Segmentation using Deep Learning

I created this project to segment customers based on their purchasing behavior, using deep learning techniques. The main goal was to identify meaningful customer segments to help businesses target their marketing and improve customer engagement strategies. Using an autoencoder for dimensionality reduction and K-Means for clustering, I was able to discover four distinct customer segments.

## Table of Contents
- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Deep Learning Model](#deep-learning-model)
- [Clustering and Results](#clustering-and-results)
- [Conclusions](#conclusions)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

## Project Overview
This project is focused on identifying customer segments by analyzing their purchasing data. By using deep learning and clustering techniques, I was able to uncover key customer behaviors, providing insights that can improve business strategies related to marketing, customer retention, and personalized sales efforts.

## Project Structure
The project is organized as follows:

```
├── customer_orders.csv          # Dataset used for the project
├── Customer Segmentation.ipynb  # Jupyter notebook with the analysis
│   ├── 1. Introduction and Problem Statement
│   ├── 2. Data Loading and Initial Exploration
│   ├── 3. Data Cleaning and Preprocessing
│   ├── 4. Feature Engineering
│   ├── 5. Deep Learning Model for Dimensionality Reduction (Autoencoder)
│   ├── 6. Extracting Encoded Data for Clustering
│   ├── 7. Clustering with K-Means
│   ├── 8. Evaluation of Clusters and Visualizations
│   ├── 9. Conclusion and Insights
│   └── 10. Future Work and Next Steps
├── README.md                    # This README file
└── LICENSE                      # MIT License file

```

## Dataset
The dataset I used comes from Kaggle, containing information about customer orders, shipping details, and products. The key features include:
- **Customer Information**: Customer IDs, segments (Consumer, Corporate), city, country, and other attributes.
- **Order Details**: Order date, sales per customer, payment types, and product categories.
- **Shipping Information**: Shipping modes, dates, and durations.

## Data Preprocessing
I cleaned the dataset through several important steps:
1. **Handling Missing Data**: Missing values were addressed using forward filling, ensuring no gaps that could affect the analysis.
2. **Correcting Shipping Durations**: I handled cases where shipping durations were negative or unreasonable.
3. **Normalization and Encoding**: To prepare the data for model input, numerical features were normalized, and categorical features were one-hot encoded.

These preprocessing steps ensured a clean and consistent dataset, ready for feature extraction and modeling.

## Feature Engineering
To help the model identify customer segments more effectively, I created new features:
- **Customer Lifetime Value (CLV)**: Measures the total value a customer has provided based on their purchase history.
- **Purchase Frequency**: Represents the number of purchases made by a customer.
- **Profit Margins**: Calculated as the ratio of profit to sales per order, helping identify more profitable customers.

## Deep Learning Model
I used an autoencoder to reduce the high-dimensional data into a compressed, lower-dimensional form. This allowed for more efficient clustering of customer behaviors while retaining important features.

The autoencoder was able to reduce the dataset to eight essential features, which captured key aspects of customer behavior. These compressed features were then used for clustering.

## Clustering and Results
After reducing the data dimensionality, I applied **K-Means clustering** to categorize customers into four distinct segments. The number of clusters was determined using the **Elbow Method** and confirmed with evaluation metrics like the **Silhouette Score**.

### The Four Customer Segments:
1. **Segment 0 (High-Value, Frequent Shoppers)**
   - Contains slightly more than 3000 customers.
   - These customers tend to make frequent and high-value purchases, contributing significantly to revenue.

2. **Segment 1 (Mid-Spending, Occasional Shoppers)**
   - Consists of around 2500 customers.
   - This group is more selective and makes purchases occasionally, but with a higher spending capacity than some other segments.

3. **Segment 2 (Price-Sensitive, Medium Engagement)**
   - The second largest group, containing around 4500 customers.
   - These customers are more price-sensitive and often make lower-value purchases. However, they still engage regularly with the business.

4. **Segment 3 (Low-Engagement, Low-Spending)**
   - The largest segment, with approximately 5000 customers.
   - This group is characterized by infrequent purchases and lower spending, often opting for budget products or waiting for discounts.

### Visualizations:
I used **Principal Component Analysis (PCA)** to reduce the clustered data into two dimensions for visualization. The resulting plots clearly showed the separation between the four segments, validating the effectiveness of the clustering approach.

These insights are critical for businesses, as they highlight different customer personas. Each segment represents a unique opportunity for targeted marketing and engagement strategies. For example, Segment 0 could benefit from loyalty programs, while Segment 3 might need price incentives to encourage more frequent purchasing.

## Conclusions
This project successfully demonstrated how deep learning and clustering can be used to uncover customer segments in a real-world dataset. By segmenting the customers into four distinct groups, businesses can better understand customer behavior and develop more targeted marketing campaigns.

## Future Work
In future iterations of this project, I aim to:
- **Experiment with Advanced Clustering Techniques**: Techniques like DBSCAN or Hierarchical Clustering could provide even more nuanced customer groupings.
- **Incorporate More Features**: Adding features like customer feedback, return rates, and web activity could provide deeper insights into customer behavior.
- **Develop Predictive Models**: Using these customer segments as input for predictive models could help forecast future customer behavior, such as churn or lifetime value.

## License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## Contact
For any inquiries, feel free to contact me:
- **Karan Zaveri**
- Email: karanzaveri92@gmail.com
