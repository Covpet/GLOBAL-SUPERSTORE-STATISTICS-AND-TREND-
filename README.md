# GLOBAL-SUPERSTORES-ADS-ASSIGNMENT
This project was done using jupyter notebook in python. Global Superstore, headquartered in New York, is a leading e-commerce retailer with a vast product range. Committed to serving its global customer base, the company offers access to over 10,000 diverse products, catering to customers from 147 countries. 

## Table of Content
- [Project Overview](Project.Overview)
- [Data Source](Data.Source)
- [Tools](Tools)
- [Project Structure](Project.Structure)
- [Data Collection](Data.Collection)
- [Data Cleaning](Data.Cleaning)
- [Methodology and Data Visualization](Methodology.and.Data.Visualization)
- [Data Documentation](Data.Documentation)
- [Exploratory Data Analysis(EDA)](Exploratory.Data.Analysis (EDA))
- [Findings](Findings)
- [Recommendation](Recommendation)
- [Conclusion](Conclusion)
- [Refrence](Reference)


## Project Overview
---
Global Superstore, a well-known online retailer with an extensive product selection, is based in New York. Dedicated to providing for its international clientele, the business serves clients in 147 nations by providing access to over 10,000 unique products. These products fall into three primary categories: furniture (including chairs), office supplies (such staples), and technology items (like smartphones). The project's goal is to gather insightful information by analyzing the Superstore dataset. These understandings will enable management to take well-informed decisions that raise profitability and performance levels overall.

## Data Soure
---
The link to the dataset which was gotten from Kaggle is provided below;

- [Download here](https://docs.google.com/spreadsheets/d/1nxESpFzWjlGDMGDVLH69xmDzIl9l6OEq/edit#gid=633280281)

- [Click here](https://www.kaggle.com/code/nishathakkar/global-superstores-customer-product-analysis/input?select=Global_Superstore2.csv)


## Tools
- Excel - Data Cleaning 
- Jupyter Notebook - Python Coding and Visualization
- Word - Documentation and Summary
- Github - Code Documentation


## Project Structure
 This project was executed following the subsequent process.

### **Data Collection**

In the first stage of the project, we focus on obtaining the Global Superstore dataset which was secondary dataset obtained from Kaggle.

### **Data Cleaning**

The Data Cleaning phase stands as a crucial component of any data analysis project. In this segment, I methodically describe the steps and methods utilized to guarantee the dataset's accuracy, dependability, and its readiness for analysis . This procedure involves validating the data, eliminating duplicates, managing missing values, and rectifying any irregularities or discrepancies found in the original data.This dataset consisted of three tables: Orders, People, and Returns. During this procedure, I noticed that the 'Postal code' field in the Order table contained approximately 80% Null values. I replaced these Null values with '0.' Furthermore, I combined the Returns table with the Order table using the VLOOKUP function in Microsoft Excel. In addition, I conducted a comprehensive validation and quality check on all rows and columns within the dataset to ensure its accuracy and integrity. The objective is to generate a tidy and well-organized dataset that serves as the foundation for our insights and visualizations, accomplished through the use of Power Query in excel and functions in python. This process involves checking the data for mistakes, removing copies, handling any missing information, and fixing any problems found. I did this using Power Query in Excel. Also, I used the code ***'print(Stores_df.isnull().sum())'*** to see how many missing pieces of information there are in each part of the data (Stores_df). When I found missing info, I used Stores_df.fillna(0, inplace=True) to fill in those gaps with the number 0. This change happened right in the original data. Next, I used print ***(Stores_df.duplicated().sum())*** to see if there were any identical entries in the data. In this case, there weren't any, so everything is good.

### **Methodology and Data Visualization**

Data Visualization plays a pivotal role in the realm of data analysis. This stage encompasses the creation of an interactive and informative dashboard using Power BI. Through this dashboard and the associated reports, I provide a comprehensive perspective on the Global Superstore sales report. My visualizations provide a more profound insight into the essential performance metrics, profitable countries, lucrative regions, subcategories, and various other metrics. By using charts, graphs, and tables, I breathe life into the data, making it easy for stakeholders to swiftly grasp the insights extracted from the dataset.

- **Reading files**:
  To read the csv file, I saved the file in my file path in my desktop folder using the function **pd.read_csv(file_path, encoding='latin1')**
- **Descriptive Statistics** :
  I used the method **.describe()** to get the descriptive statistics for the column variables. To get my skewness and Kurtosis, I used the function **.skew()** and **.kurtosis()** from the python library **scipy.stats**
- **Relational Graph** : I used a line chart for this to compute the trend of sales, profit and shipping cost over time.
- **Categorical Graph** : I used a pie and bar chart to get the top 3 countries by total profit in 2014, subcategories with highest average shipping cost, Top 10 customer by profit, Profitability of tables in southeast Asia by country, Average profit by product subcategory in Australia.
- **Statistical Graph** : I used a heatmap to compute the correlation matrix among the numerical variables Sales, quantity, Discount, Profit Shipping cost and boxplot to generate the top 3 product sub-categories.

 
### **Data Documentation**

Following the conclusion of the analysis, I recognize the significance of effectively conveying the discoveries and suggestions. For this purpose, I've established an extensive documentation repository on GitHub. This documentation serves as a valuable reference that elucidates the insights I've uncovered from the dataset, providing comprehensive explanations of these insights and delivering a thorough overview of the recommendations. It equips the leadership of Global Superstore with the insights necessary to make informed decisions with the goal of enhancing overall performance and profitability.


## Exploratory Data Analysis(EDA)
Exploratory Data Analysis (EDA) is a crucial step in our approach to the Global Superstore dataset. It involves diving deep into the data to answer essential questions that underpin our analysis and decision-making. These questions are 
  
- **Question 1**:
  
Which three nations brought in the most money overall for Global Superstore in 2014?
- **Question 2**:
  
Determine which three subcategories in the US have the greatest average shipping costs.
- **Question 3**:
  
Evaluating the profitability (i.e., total profit) of the United Kingdom in 2014. In what way does it differ from other nations?
- **Question 4**:
  
Determine which product subcategory in Southeast Asia is the least profitable. Is there a particular Southeast Asian nation where Global Superstore ought to cease carrying the subcategory? 
- **Question 5**:
  
Evaluate the long-term trends in sales, profit, and transportation expenses. In different storylines 
- **Question 6**:

Determine the correlation between the sales dataset's numerical variables. 
- **Question 7**:
  
In terms of average profit, which American city is the least profitable? Eliminate the cities with fewer than ten Orders for this study. b) Why is the average profit in this city so low? 
- **Question 8**:
  
What do the most valuable clients buy, and who are they?



## Data Analysis 

- **Question 1**:

Within the financial landscape of Global Store for the year 2014, three countries emerged as significant drivers of profit: the United States, China, and India. The United States stood out with an impressive profit of $39,936.85, underscoring its crucial role as a major revenue generator for the company. China secured the second position, making a substantial contribution of $8,421.33 to the overall profits. The rapid growth of the Chinese market played a pivotal role in achieving this. India, in the third position, also made a notable contribution with a profit of $7,330.95. This emphasizes the increasing influence of the Indian market on Global Store's financial performance. Collectively, these three countries played a central role in shaping the profitability of Global Store in the year 2014. The given code in question 1 defines a function called **`plot_top_countries_profit` that takes a DataFrame `Stores_df` as input. This function performs the following steps:
1. Converts the 'Order Date' column in the DataFrame to datetime data type using `pd.to_datetime` function from the pandas package.
2. Filters the data for the year 2014 using boolean indexing.
3. Groups the filtered data by country and calculates the total profit for each country using the `groupby` and `sum` functions from pandas.
4. Creates a pie chart to visualize the top 3 countries by total profit in 2014 using `plt.pie` and `plt.show` functions from the matplotlib package.
The function `plot_top_countries_profit` is then called with a DataFrame `Stores_df` as an argument. The code uses the `pandas` package for data manipulation and the `matplotlib.pyplot` module for data visualization.

- Here is a breakdown of the countries and products that have contributed the most to our profitability

*Most Profitable product in United States and their profits*

|Product Name |Profit|
|----------------|-------------------|
|canon imageCLASS 2200 Advanced copier|25,199.993|
|fellowes PB500 electric plastic Comb Binding Machine with Manual Bind|7,753.04 |
|Hewlett Packard Laserjet 3310 Copier| 6,983.88 |
|Total| 39,936.85|

*Most Profitable Product In China and their Profits*

|Product Name |Profit|
|------------------|--------------------|
|Sharp wireless Fax, Digital|2,894.10|
|Hp Copy Machine, Color|2,855.13|
|Samsung Smart Phone, VolP|2,672.10|
|Total|8,421.33|

|*Most Profitable Product In India and their Profits*

|Product Name |Profit|
|--------|--------|
|Sauder Classic Bookcase,Traditional        |2,903.58|
|Apple Smart Phone, with Caller ID          |2,817.99|
|Cisco Smart Phone with Caller ID   |1,609.38|
|Total|7,330.95|

![Dashboard](PIE-CHART.PNG)

![PIE CHART](https://github.com/Covpet/GLOBAL-SUPERSTORES-ADS-ASSIGNMENT/assets/148041100/a7e21921-9f6e-4f80-9331-6de771599a3f)


- **Question 2**

To gain valuable insights into the shipping dynamics within the United States and understand how these specific product groups impact the business's financial performance, I needed to delve deeper. When examining shipping costs in the United States, it's intriguing to discover that three particular subcategories stood out due to their high average shipping expenses. These subcategories include Copiers, Machine, and Tables, and they played a central role in shaping the dynamics of shipping costs. Among these, Copiers took the lead as the subcategory with the highest average shipping cost, registering an impressive 165.29. Machines secured the second position with an average shipping cost of 132.25 % while tables had the 3rd highest average shipping cost with about 69.95. The cost of shipping these items stands as a significant factor to consider when assessing profit margins and making logistical decisions.The **`plot_top_shipping_costs`** function in th jupyter documentation for question 2 creates a bar chart to visualize the average shipping cost for the top n subcategories in a specific country. It takes a DataFrame containing shipping cost data, a country name, and an optional parameter n. The function filters the data for the specified country, calculates the average shipping cost for each subcategory, selects the top n subcategories with the highest average shipping cost, and then creates a bar chart to visualize this information using pandas for data manipulation and matplotlib for visualization.

![Dashboard](BAR-CHART.PNG)

![BAR CHART](![BAR CHART](https://github.com/Covpet/GLOBAL-SUPERSTORES-ADS-ASSIGNMENT/assets/148041100/cb9b2616-e5fb-4459-8eea-63ae6097dc4f))


- **QUESTION 3**
  
The `calculate_and_compare_profit` function performs the following operations on a given DataFrame containing profit data:

1. It filters the data for the United Kingdom.
2. It calculates the total profit for the United Kingdom in the year 2014 as a sum.
3. It groups the data by country and calculates the total profit for each country.
4. It sorts the total profit by country in descending order.
5. It prints the total profit for the United Kingdom in 2014 and compares it to the total profits of other countries.

The function provides a convenient way to analyze and compare the total profits of different countries, with a specific focus on the United Kingdom. This can be useful for gaining insights into the performance of different countries in terms of profitability.The function is designed to take a DataFrame as input and does not return any value, but rather performs the specified operations and prints the results. The next sell under question 3 selects the top 20 countries by profit from the DataFrame `total_profit_by_country` and assigns it to the variable `top_countries`. It then creates a list of colors for the bar graph, using 'skyblue' for countries other than the United Kingdom and 'orange' for the United Kingdom. Next, it creates a horizontal bar graph to visualize the total profits of the selected countries. The figure size is set to (10, 6) for the bar graph. The bar graph displays the total profit for each country, with the United Kingdom highlighted in orange and other countries in sky blue. The x-axis is labeled as 'Total Profit', the y-axis is labeled as 'Country', and the title of the bar graph is set as 'Top 20 Countries by Total Profit'. Finally, the bar graph is displayed. This provides a clear visual comparison of the total profits of the top countries, with special emphasis on the United Kingdom. It was obeserved that uk has a total profit of 111900.15 in 2014 which made them the 4th highest profitable country in the year 2014. To get the top 10 most profitable products in United kingdom, the next cell Analyzes the profitability of products in the United Kingdom is the analyze_uk_profitability(Stores_df) function. It then Filter the dataframe to include only rows where the country is the United Kingdom, Calculate the average discount, shipping cost, quantity, and sales for each product, Sort the dataframe by profitability (e.g., sales) in descending order and display only the top 10 products and Display the resulting dataframe with the rows as the product names. From the analyze function in the python code, it was seen that Motorola Smart Phone, Cordless has the highest shipping cost and sales which was 656.730 and 5785.020 respectively which made it more profitable followed by Barricks Conference Table, Fully Assembled  and KitchenAid Refrigerator, Black. From the analysis, due to high demand in quantity of Motorola Smart Phone, Cordless, they had more sales which made it more profitable compared to other countries.

- **QUESTION 4**
  
The `visualize_profitability` function creates a heatmap graph to visualize the profitability of product subcategories in Southeast Asia. It performs the following steps:

1. Filters the input DataFrame to include only rows where the region is Southeast Asia.
2. Calculates the profitability for each product subcategory within Southeast Asia.
3. Identifies the least profitable product subcategory in Southeast Asia.
4. Creates a heatmap graph to visualize the profitability of product subcategories in Southeast Asia using the seaborn library.
5. Displays the heatmap graph and prints the least profitable product subcategory in Southeast Asia.

The function provides a clear visualization of the profitability of product subcategories in Southeast Asia and identifies the least profitable subcategory, allowing for quick insights into the performance of different product categories within the region. The analysis covers a set of Southeast Asian countries, including Malaysia, Indonesia, Philippines, Thailand, Vietnam, Cambodia, Singapore, and Myanmar. In these countries, a diverse array of subcategories were available, encompassing Phones, Copiers, Appliances, Bookcases, Machines, Chairs, Storage, Binders, Furnishing, Labels, Art, Fasteners, Paper, Supplies, Accessories, and Tables. Interestingly, among all these subcategories, 'Accessories' emerged as the least profitable in the Southeast Asian region, resulting in a negative mean profit of -46 . On the contrary, 'Phones' proved to be the most profitable subcategory, yielding a mean profit of 300 followed by . This shows that South East Asia does not really invest in Accesories probably due to the religion or tradition. The `visualize_profitability` function creates a heatmap graph to visualize the profitability of product subcategories in Southeast Asia. It performs the following steps:

1. Filters the input DataFrame to include only rows where the region is Southeast Asia.
2. Calculates the profitability for each product subcategory within Southeast Asia.
3. Identifies the least profitable product subcategory in Southeast Asia.
4. Creates a heatmap graph to visualize the profitability of product subcategories in Southeast Asia using the seaborn library.
5. Displays the heatmap graph and prints the least profitable product subcategory in Southeast Asia.

The function provides a clear visualization of the profitability of product subcategories in Southeast Asia and identifies the least profitable subcategory, allowing for quick insights into the performance of different product categories within the region. Considering the significant loss associated with 'Accesories' in South East Asia, it might be advisable to reconsider the supply of this subcategory by Global Superstore to prevent further financial setbacks. The function identify_lowest_profitability_country(Stores_df, subcategory) then Identifies the country in Southeast Asia with the lowest profitability for a specific subcategory, Filter the dataframe to include only rows where the region is Southeast Asia, Calculate the profitability for the specified subcategory in each country, Identify the country with the lowest profitability for the specified subcategory, Create a bar plot to visualize the profitability of the specified subcategory in each country. Iw was observed that The country in Southeast Asia with the lowest profitability for the subcategory 'Tables' is: Thailand.

- **QUESTION 5**
  
The provided code performs the following operations:

1. It converts the 'Order Date' and 'Ship Date' columns in the DataFrame `Stores_df` to datetime format with error handling using the `pd.to_datetime` function. The `errors='coerce'` parameter is used to handle any errors by converting problematic values to NaT (Not a Time).

2. It then groups the data by 'Order Date' and aggregates based on the mean of 'Sales', 'Profit' and 'Shipping cost' respectively resulting in a new DataFrame called `grouped_data`.

3. It defines a function called `plot_sales_trend`, `plot_profit_trend` and `plot_shippingcost_trend` that plots the trend of sales over time using the matplotlib library. The function creates a line plot with 'Order Date' on the x-axis and 'Sales', 'Profit' and 'Shipping Cost' respectively for each plot on the y-axis, and includes a title, axis labels, legend, and x-axis rotation for better readability.

4. Finally, it calls the `plot_variables_trend` function to visualize the trend of sales, profit and shipping cost respectively in the pictures below over time.

This code to question 5 effectively converts date columns to datetime format, aggregates the data based on mean sales, profit and shipping cost and then visualizes the the trend over time, providing a clear representation of the considered variables in the dataset. 

![Dashboard](LINE-CHART1.PNG)

![LINE CHART1](![LINE CHART1](https://github.com/Covpet/GLOBAL-SUPERSTORES-ADS-ASSIGNMENT/assets/148041100/ec95a235-d489-4c96-a85f-8a9c969ec7dd))

![Dashboard](LINE-CHART2.PNG)

![LINE CHART2](![LINE CHART2](https://github.com/Covpet/GLOBAL-SUPERSTORES-ADS-ASSIGNMENT/assets/148041100/4a6f45ad-c848-4b00-9581-80060dc6b273))

![Dashboard](LINE-CHART3.PNG)

![LINE CHART3](![LINE CHART3](https://github.com/Covpet/GLOBAL-SUPERSTORES-ADS-ASSIGNMENT/assets/148041100/d25b7206-8cd0-4862-9570-cef145fffba8))

The line chart shows that around the fourth month of the year 2011, it was recorded to have the highest sales over time, it decreased later on and then remained stable, another drastic increase was recorded in the early years of 2013 and 2014, this shows the how the trend of sales has been flunctuating over time. From the profit trend line chart, it was seen that most of the years was recorded decrease especially the year 2012 had a drastic decrease in the population but in the year 2014 ending it was recorded to have the highest increase in profit, this shows that there was a recent development in the profit of goods. The trend of shipping cost in the line chart from the year 2011 to the year 2014 ending was filled with upward and downward trends resulting into a large flunctuation but also the year 2014 ending had the highest shipping cost.

- **QUESTION 6**
  
The code to question 6 on the jupyter notebook defines a function `plot_correlation_matrix` that creates a heatmap of the correlation matrix for selected columns of a dataframe. It uses the `seaborn` and `matplotlib` libraries to create the heatmap and plot the correlation matrix. The function takes a dataframe `Stores_df` and a correlation method as input, selects specific columns from the dataframe, and then plots the correlation matrix using the specified method. It then calls the method for pearson and kendall to plot separate heatmap, the darker the colour, the higher the correlation, the fainter the colour, the lower the correlation. Pearson correlation is suited for measuring the strength of a linear relationship between two continuous variables, while Kendall correlation is more appropriate for assessing the degree of association between two variables when the data are ordinal, ranked, or not normally distributed. The choice between the two depends on the nature of the data and the type of relationship being studied. From the pearson heatmap, it was seen that sales has a strong positive correlation with shipping cost with exactly 0.77, while sales has a weak positive correlation with quantitty and profit which is 0.31 and 0.48 respectiely, then it has a negative correlation with discount. Also, quantity has a weak positive correlation with profit and shipping cost while it has a negative correlation with discount. Discount has a negative correlation with shipping cost and profit while profit and shipping cost has a weak positive correlation, Overall it shows that sales and shipping cost has the highest positve correlation among other variables This relationship suggests that higher sales volumes may lead to increased shipping expenses, potentially due to higher shipping volumes, larger package sizes, or expedited shipping options chosen by customers.
On the Other hand, using the kendall correlation there were not more differnces with that of pearson, the observed difference was that in pearson heatmap, discount and quantity has a negative correlation while in kendall they are postive, it might be due to some reasons like treatment of data distribution, linearity versus rank ordering, sensitivity to outliers, sample size considerations, and interpretability, necessitating careful selection based on the specific data and research context. The visuals is displayed in the python code.

- **QUESTION 7**

This function least_profitable_city_in_us(Stores_df) in question 7 in th python code identifies the least profitable city in the United States by filtering the dataframe to include only rows where the country is the United States, calculating the number of orders for each city, discarding cities with less than 10 orders, calculating the average profit for each city, and then identifying the least profitable city .Among the Cities in the United States, Lancaster stands out due to its lowest profit, resulting in a significant mean loss of -157.37. A closer examination uncovers that Lancaster grapples with elevated shipping costs combined with limited discounts.This function also analyzes attributes for the city of Lancaster in a dataframe to identify factors contributing to its least profitability. It filters the dataframe to include only rows where the city is Lancaster, selects relevant attributes for analysis, and generates a table of attributes for the city of Lancaster. The high shipping expenses can dissuade customers from making purchases because of the higher selling prices, prompting them to seek local alternatives. Conversely, offering minimal discounts may discourage repeat buying, leading to financial deficits.To enhance profitability in Lancaster, it is advisable for the company to reassess its pricing strategy. This might involve exploring ways to reduce shipping costs or providing more enticing discounts to incentivize customers to make more frequent purchases. A deep understanding of the local market dynamics and customer preferences in lancaster is essential in formulating a strategy that can reverse the current situation and reinstate profitability. 

- **QUESTION 8**

The code defines a function `analyze_most_valuable_customers` that calculates the total purchase amount for each customer, identifies the top 10 most valuable customers, determines the products purchased by these customers, merges the data to create a table, drops duplicate rows, and then prints a table showing the most valuable customers, the products purchased, and the countries they belong to.
  
Below is a list of our most profitable customers and what they purchase, as it is seen in the tables, it was obvious that the top 6 were fronm United States as it was recorded that United states has the highest profitability


|Name of Customer|Products they purchased|Country|
|----------------|-----------------------|-------|
|Sean Miller|SAFCO Commercial Wire Shelving, Black|United State|
|Tamara Chand|Canon imageCLASS 2200 Advanced Copier|United State|
|Raymond Buch|Boston 1645 Deluxe Heavier-Duty Electric Penci...|United State|
|Tom Ashbrook|Polycom CX600 IP Phone VoIP phone|United State|
|Adrian Barton|GBC Ibimaster 500 Manual ProClick Binding System|United State|
|Ken Lonsdale|GBC Recycled Regency Composition Covers|United State|



## Findings

- The 2014 financial review emphasized how important the US, China, and India are to Global Store's profitability and how important a role they play in determining the company's financial environment.
  
- A review of the best-selling products in various areas offered insightful information on profitable products, enabling well-informed choices about product lines and advertising tactics.
  
- An analysis of shipping dynamics in the US indicated significant effects of particular product categories on shipping expenses, pointing to opportunities for cost-efficiency enhancements and optimization.
  
- A study of product profitability in the UK revealed the best-performing items and the profits that went along with them, offering information on customer preferences and market demand.
  
- Strengths and weaknesses were identified by the heatmap analysis of Southeast Asian product subcategories, which helped inform strategic choices for product diversification and market expansion.


## Recommendations

Investigate joint ventures or partnerships to improve consumer involvement and market penetration.
  
- Direct resources toward growing and promoting the most profitable product lines.
  
Investigate other shipping options or joint ventures with logistics companies to reduce costs and optimize operations.
  
- Keep an eye on pricing tactics and make adjustments as needed to optimize profits while maintaining market competitiveness.
  
- Make marketing and promotional investments in underperforming subcategories in order to boost customer involvement and visibility.
  
Investigate joint ventures or partnerships with regional companies to improve brand awareness and market penetration in Southeast Asia.


## Conclusion

All things considered, the thorough studies offer insightful information about important markets, product performance, and operational effectiveness, empowering Global Store to make data-driven choices for profitable and strategic expansion. In the cutthroat world of e-commerce, Global Store can improve its position in the market, maximize operational effectiveness, and spur long-term growth by utilizing these insights and putting focused initiatives into place. The research, which focuses on significant markets, product performance, and operational efficacy, can help Global Store determine its strategic course. Global Store can maintain its position as a global leader in e-commerce by using these data to guide focused strategies in product diversification, market expansion, and logistics optimization. This will benefit customers while maximizing profitability and operational performance.






## Reference 
[Link to Dataset](https://docs.google.com/spreadsheets/d/1nxESpFzWjlGDMGDVLH69xmDzIl9l6OEq/edit#gid=633280281)
