 # Sales-Dashboard

## Problem Statement

The CEO and CMO of an online retail store need insights from their revenue and sales data to guide strategic decisions. They have specific requirements:

- 2011 Revenue Trends: The CEO seeks a monthly revenue analysis for 2011 to identify seasonal trends and improve forecasting for the next year.

- Top 10 Countries by Revenue (Excluding the UK): The CMO wants to identify the top 10 revenue-generating countries, excluding the UK, along with the quantity of products sold.

- Top 10 Customers by Revenue: The CMO needs a visual ranking of the top 10 customers by revenue to focus on retention strategies for high-value customers.

- Global Demand Analysis (Excluding the UK): The CEO wants to identify regions with the highest product demand (excluding the UK) to inform expansion strategies.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a xlsx file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : Check data types for each column and adjust as needed. For example, convert CustomerID to text since it's a unique identifier.
- Step 5 : Ensured that numerical fields like Unit Prices and Quantity are correctly formatted in decimal and without negative values. 
- Step 6 : Categorize geographical data, country column, to facilitate accurate visualization and mapping analysis
- Step 7 : Apply data transformations as needed. This included removing negative values in Unit Prices and Quantity columns and ensuring all data was in the correct format. 

- Step 8 : Identified the key metrics and the appropriate level of detail required to directly address the CMO and CEO's questions.  
- Step 9 : Chose a consistent color format in advance to maintain visual uniformity and enhance the professionalism of the report.
- Step 10 : Create visualizations to analyze the data:

    - Line Charts: Visualized the revenue trend across 2011, with drill-down features enabled for users to analyze performance by day or week for deeper insights.
    - Column Charts: Displayed the top 10 revenue-generating customers in descending order, from highest to lowest.
     - Map Visualization: Used bubble sizes to represent demand across regions, where larger bubbles indicate higher demand.
     - Bar Charts and Cards: Created visuals to compare revenue and quantity sold by country for a comprehensive analysis. 
        
- Step 11 : New measure was created to find total revenue collected.

Following DAX expression was written for the same,
        
        Revenue = SUMX('Online Retail', 'Online Retail'[UnitPrice] * 'Online Retail'[Quantity])
        
A card visual was used to represent Revenue collected.


![revenue](https://github.com/user-attachments/assets/4f389c09-60cb-46e5-9755-52340137911c)
- Step 12: Conducted a final review of the visualizations to ensure accuracy and that they effectively answered the CMO and CEO's questions, making adjustments as necessary.

 - Step 13 : The report was then published to Power BI Service.




# Snapshot of Dashboard 

![sales-dashboard](https://github.com/user-attachments/assets/b77cf6a9-c296-4666-9cd5-52f46d4324d7)
 

# Insights

A multiple page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Line Chart


![question1](https://github.com/user-attachments/assets/ff07c65b-e7e8-4524-aeec-af45cdddc6d1)

   

The analysis reveals that revenue remains fairly constant during the first eight months of the year, averaging around $685k. However, a notable increase in revenue begins in September, where there is a 40% rise compared to the previous month. This upward trend continues through November, reaching a peak of $1.5 million, the highest for the entire year. Unfortunately, the data for December is incomplete, making it impossible to draw conclusions for that month. Overall, this analysis suggests that the retail store's sales are significantly impacted by seasonality, particularly during the last four months of the year, likely driven by year-end consumer spending and holiday-related sales.
           
Given the evident seasonal boost, it's crucial to ensure that operations, marketing, and inventory are aligned to capitalize on this momentum.

    Note that while December's revenue appears low, a closer look at the daily data reveals that we only 
    have data for 9 days. This suggests that revenue is actually performing well, and the apparent 
    drop  is due to incomplete data.Look below
![Screenshot (73)](https://github.com/user-attachments/assets/1a04906e-0669-498f-8831-57ba8418ed3d)



### [2] Bar Chart

![question2](https://github.com/user-attachments/assets/074c0719-351c-4e45-a6f0-1f7208e52b62)
The Netherlands leads in both revenue and quantity sold, followed by Ireland, Germany, France, Australia, and others. However, Spain and Belgium stand out with lower sales volumes but impressive revenue, likely due to premium products or higher pricing.

 By understanding what’s driving success in Spain and Belgium, we can replicate it in other markets and apply these strategies to boost revenue in regions with high sales but lower earnings
   
  
  ### [3] Column Chart 
  

![question3](https://github.com/user-attachments/assets/97f0ae17-f7ad-4f0e-b0e2-ec4111ebaf58)
      
From our chart, we can see the top 10 revenue-generating customers, starting with CustomerID 14646 down to CustomerID 12346

This will help us strengthen relationships with the top clients, reduce dependency by diversifying our customer base, and identify similar high-value prospects for targeted growth

 ### [4] Mapping Visualization
 
 ![question4](https://github.com/user-attachments/assets/29afe395-0ab2-48c8-b9bf-7fd3a307f34d)

In summary, our analysis shows key opportunities we can leverage for future success. We should focus on maximizing the strong seasonal trends in the last quarter and apply the successful premium strategies from Spain and Belgium to other markets. Strengthening our top customer relationships and expanding into high-demand regions will also help ensure sustainable growth. These insights will guide our next steps as we refine our strategies.
 
