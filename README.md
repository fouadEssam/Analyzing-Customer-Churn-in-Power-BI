# Analyzing-Customer-Churn-in-Power-BI
Data Camp Project
# Defining churn 
A good definition is the one from Investopedia: “The churn rate, also known as the rate of attrition or customer churn, is the rate at which customers stop doing business with an entity.” Churn reminds me of the leaking bucket dilemma. You can add additional water to the bucket (or new clients in this example), but your overall revenue will not improve if existing customers leave. Because retaining customers is simpler than attracting new ones, reducing churn is a top aim for many businesses.

![image](https://github.com/user-attachments/assets/42639867-c65c-496c-8bc8-46fb3ba66f67)


#### Goal:
To analyze and identify the reasons for customer churn at Databel, a fictitious telecom provider, and provide insights to reduce the churn rate.

#### Problem:
Customer churn is when customers stop doing business with Databel. The goal is to understand why customers are leaving.

#### Solution:
1. **Defining Churn**:
   - Churn rate is the percentage of customers who stop doing business with Databel.
   - Example: If 10 out of 100 customers leave, the churn rate is 10%.

2. **Data Overview**:
   - Our dataset comprises a comprehensive table with 29 columns, each representing valuable customer information. I have a snapshot of the database at a specific moment, which means there is no time dimension.
   - Customer ID|Churn Label|Account Length (months)|Local Calls|Local Mins|Intl Calls|Intl Mins|Intl Plan|Extra International Charges|Customer Service Calls|Avg Monthly GB Download|Unlimited Data Plan|Extra Data Charges|State|Phone Number|Gender|Age|Under 30|Senior|Group|Number of Customers in Group|Device Protection and Online Backup|Contract Type|Payment Method|Monthly Charge|Total Charges|Churn Category|Churn Reason.
  
    ![image](https://github.com/user-attachments/assets/82030ac5-a5f6-4b7a-9be1-c35da623ccf3)


3. **Data Check**:
   - Ensure no duplicate customer IDs to avoid double-counting.
     
     ![image](https://github.com/user-attachments/assets/ca25a018-5e43-4410-8f17-28430481d41f)


4. **Calculating Churn**:
   - Convert `Churn Label` to a binomial column (1 for churned, 0 for not churned).
     
     ![image](https://github.com/user-attachments/assets/7ee7e8e8-e8ca-47a2-ba6e-ea3251ae58fa)
   - Create a measure for the number of churned customers
     ![image](https://github.com/user-attachments/assets/70a237f1-5afc-44a0-b0c6-f3170b41173d)

   - Calculate the churn rate, which is 26.86%.
     
  ![image](https://github.com/user-attachments/assets/c210e54d-ff3a-4006-ae84-5e53879242a0)


5.# Insights:
   - Analyze churn rate by state to identify regions with high churn rates.
   - Example: California has a high churn rate of 63.24%.
     
![image](https://github.com/user-attachments/assets/5ef255f8-a660-41a3-8c1f-2a9c47971050)


- The average churn rate is around 27%.<br>
  ![image](https://github.com/user-attachments/assets/f05753be-1760-418a-b507-7ea7e6dab327)

-Databel offers group contracts to customers from the same household. The advantage for the customer is a discounted rate, while it’s a great way for Databel to grow its customer base. My objective is to determine whether consumers who belong to a group have a lower phone bill and whether this has an effect on churn.

![image](https://github.com/user-attachments/assets/64595a13-775d-42f2-989c-3aecb9d01734)<br>
![image](https://github.com/user-attachments/assets/a5ffbb1b-32ee-4332-9c80-846f9af76c0f)

-Additionally, a clustered bar chart showcases churn rate by contract category and gender.

![image](https://github.com/user-attachments/assets/b06c05ac-2e73-43f7-abfa-94bb199b212d)

-I’ve compared these insights with churn rate through a clustered bar chart:

![image](https://github.com/user-attachments/assets/e960e38b-e6fd-4026-b55f-221abb056fa1)

- aslo I've compared it with Payment methods<br>
![image](https://github.com/user-attachments/assets/04e2bcff-cc76-408d-b514-934ba42ee472)

# Investigating Churn Reasons:
   - Top reasons for churn:
     - Competitor made a better offer.
     - Competitor had better devices.
     - Attitude of support person.
       
![image](https://github.com/user-attachments/assets/81faf531-ba00-496c-9d26-45a4e88bfaf8)

   - Group reasons into categories like "Price" and "Competitor".<br>
![image](https://github.com/user-attachments/assets/6ecbb09e-c978-40ab-a480-48e25680d44f)<br>

#  Some Recommended Strategies
### 1. Competitor Made a Better Offer
**Solution: Enhance Value Proposition**
- **Competitive Pricing**: Regularly review and adjust pricing strategies to remain competitive.
- **Promotions and Discounts**: Offer targeted promotions and discounts to retain existing customers and attract new ones.
- **Loyalty Programs**: Implement or enhance loyalty programs to reward long-term customers with exclusive benefits.

### 2. Competitor Had Better Devices
**Solution: Improve Product Offerings**
- **Partnerships with Device Manufacturers**: Collaborate with leading device manufacturers to offer the latest and most popular devices.
- **Device Upgrade Programs**: Introduce programs that allow customers to upgrade their devices more frequently.
- **Bundled Offers**: Create attractive bundles that include devices and service plans at a discounted rate.

### 3. Attitude of Support Person
**Solution: Enhance Customer Service**
- **Training Programs**: Invest in regular training for customer support staff to improve their communication and problem-solving skills.
- **Customer Feedback**: Implement a system to collect and act on customer feedback regarding their support experiences.
- **Support Metrics**: Monitor key support metrics (e.g., response time, resolution time, customer satisfaction scores) and set improvement targets.

By focusing on these areas, Databel can improve customer satisfaction and reduce churn rates. Would you like more detailed strategies or examples for any of these solutions?
7. **Geospatial Analysis**:
   - Leverage Power BI's mapping features to visualize churn rates by geographic regions.


#### Methodology:
1. **Data Collection**:
   - Import data into Power BI from Databel's customer database.

2. **Data Cleaning**:
   - Use Power BI's data transformation tools to remove duplicates and handle missing values.

3. **Data Transformation**:
   - Convert categorical columns (e.g., `Churn Label`) into numerical formats using Power BI's DAX functions.

4. **Exploratory Data Analysis (EDA)**:
   - Utilize Power BI's visualization capabilities to understand data distribution and identify patterns.

5. **Churn Rate Calculation**:
   - Create measures in Power BI to calculate the overall churn rate and segment it by different dimensions (e.g., state, customer demographics).

6. **Root Cause Analysis**:
   - Use Power BI's visualizations to identify and analyze the main reasons for churn.

#### Tools Used:
- **Power BI**: For data import, cleaning, transformation, analysis, visualization, and dashboard creation.

