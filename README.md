# E-Commerce-Marketing-and-Shopping-EDA-Hypothesis-Testing-with-Python

## Objective
In the rapidly evolving world of e-commerce, understanding customer behavior and the factors influencing purchase decisions is critical for optimizing user experience and driving business growth. This project aims to leverage two comprehensive datasets to conduct a detailed Exploratory Data Analysis (EDA) and perform hypothesis testing to uncover actionable insights.

The first dataset contains information on customers visiting the shopping site, including their engagement across different page categories, time spent, and session-specific behaviors. The second dataset includes demographic, purchase, and marketing details about the customers.

The goal is to:

Analyze User Behavior: Understand how users interact with the site, including time spent on pages, bounce rates, and engagement with specific categories.

Identify Influencing Factors: Investigate demographic, marketing, and behavioral features that impact purchase decisions.

Test Hypotheses: Formulate and test data-driven hypotheses to validate assumptions and identify opportunities for optimization.

This analysis will provide valuable insights into user behavior and recommend strategies to enhance customer engagement, improve conversions, and optimize e-commerce performance.


## Data Description for E-commerce -python EDA & Hypothesis testing

### Shopping dataset
Column Descriptions:

● Administrative: This is the number of pages of this type (administrative) that the user
visited. Eg: account, addresses, cart, orders etc

● Administrative_Duration: This is the amount of time spent in this category of pages.

● Informational: This is the number of pages of this type (informational) that the user visited.

● Informational_Duration: This is the amount of time spent in this category of pages.

● ProductRelated: This is the number of pages of this type (product related) that the user
visited.

● ProductRelated_Duration: This is the amount of time spent in this category of pages.

● BounceRates: The percentage of visitors who enter the website through that page and exit
without triggering any additional tasks.

● ExitRates: The percentage of pageviews on the website that end at that specific page.

● PageValues: The average value of the page averaged over the value of the target page
and/or the completion of an eCommerce transaction.

More information about how this is calculated

● SpecialDay: This value represents the closeness of the browsing date to special days or
holidays (eg Mother's Day or Valentine's day) in which the transaction is more likely to be
finalized. More information about how this value is calculated below.

● Month: Contains the month the pageview occurred, in string form.

● OperatingSystems: An integer value representing the operating system that the user was
on when viewing the page.

● Browser: An integer value representing the browser that the user was using to view the
page.

● Region: An integer value representing which region the user is located in.

● TrafficType: An integer value representing what type of traffic the user is categorized into.

● VisitorType: A string representing whether a visitor is New Visitor, Returning Visitor, or
Other.

● Weekend: A boolean representing whether the session is on a weekend.

● Revenue: A boolean representing whether or not the user completed the purchase.

The 'Revenue' attribute can be used as the class label. Of the 12,330 sessions in the dataset,
84.5% (10,422) were negative class samples that did not end with shopping, and the rest (1908)
were positive class samples ending with shopping.

"Administrative", "Administrative Duration", "Informational", "Informational Duration", "Product
Related" and "Product Related Duration" represent the number of different types of pages
visited by the visitor in that session and total time spent in each of these page categories.
The values of these features are derived from the URL information of the pages visited by the
user and updated in real time when a user takes an action, e.g. moving from one page to
another.

The "Bounce Rate", "Exit Rate" and "Page Value" features represent the metrics measured by
"Google Analytics" for each page in the e-commerce site. The value of "Bounce Rate" feature
for a web page refers to the percentage of visitors who enter the site from that page and then
leave ("bounce") without triggering any other requests to the analytics server during that
session.

The value of "Exit Rate" feature for a specific web page is calculated as for all pageviews to the
page, the percentage that were the last in the session. The "Page Value" feature represents the
average value for a web page that a user visited before completing an e-commerce transaction.
The "Special Day" feature indicates the closeness of the site visiting time to a specific special
day (e.g. Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized
with transaction.

The value of this attribute is determined by considering the dynamics of e-commerce such as
the duration between the order date and delivery date. For example, for Valentina’s day, this
value takes a nonzero value between February 2 and February 12, zero before and after this
date unless it is close to another special day, and its maximum value of 1 on February 8.

The dataset also includes operating system, browser, region, traffic type, visitor type as
returning or new visitor, a Boolean value indicating whether the date of the visit is weekend, and
month of the year.

### Campaign dataset

Column Details:

● ID: Customer's Unique Identifier

● Year_Birth: Customer's Birth Year

● Education: Customer's education level (Graduation, Master, PhD, 2n Cycle(Diploma), Basic)

● Marital_Status: Customer's marital status

● Income: Customer's yearly household income

● Kidhome: Number of children in customer's household

● Teenhome: Number of teenagers in customer's household

● Dt_Customer: Date of customer's enrollment with the company

● Recency: Number of days since customer's last purchase

● MntWines: Amount spent on wine in the last 2 years

● MntFruits: Amount spent on fruits in the last 2 years

● MntMeatProducts: Amount spent on meat in the last 2 years

● MntFishProducts: Amount spent on fish in the last 2 years

● MntSweetProducts: Amount spent on sweets in the last 2 years

● MntGoldProds: Amount spent on gold in the last 2 years

● NumDealsPurchases: Number of purchases made with a discount

● NumWebPurchases: Number of purchases made through the company's web site

● NumCatalogPurchases: Number of purchases made using a catalogue

● NumStorePurchases: Number of purchases made directly in stores

● NumWebVisitsMonth: Number of visits to company's web site in the last month

● AcceptedCmp1: 1 if customer accepted the offer in the 1st campaign, 0 otherwise (Target
variable)

● AcceptedCmp2: 1 if customer accepted the offer in the 2nd campaign, 0 otherwise (Target
variable)

● AcceptedCmp3: 1 if customer accepted the offer in the 3rd campaign, 0 otherwise (Target
variable)

● AcceptedCmp4: 1 if customer accepted the offer in the 4th campaign, 0 otherwise (Target
variable)

● AcceptedCmp5: 1 if customer accepted the offer in the 5th campaign, 0 otherwise (Target
variable)

● Complain: 1 if customer complained in the last 2 years, 0 otherwise

● Country: Customer's location

This is a CSV file of observations (customers) with variables related to marketing data. More
specifically, the variables provide insights about:

● Customer profiles

● Products purchased

● Campaign success (or failure)

● Channel performance


## Recommendations Based on the EDA & Hypothesis Testing(Shopping dataset):

### 1. User Engagement and Content Optimization:

1. Enhance Engagement for Non-Revenue Users:
Investigate why non-revenue users have lower engagement levels. Improve product-related content to keep them on the site longer and guide them toward purchases.

2. Focus on Product-Related Pages:
Users who generate revenue spend more time on product-related pages. Enhance these pages with personalized recommendations, engaging visuals, and detailed descriptions.

3. Monitor and Reduce Bounce/Exit Rates:
Regularly track these rates to identify underperforming pages. Conduct A/B testing to improve retention and reduce drop-offs.

### 2. Session Length and Conversion Strategies:

1. Leverage Long Session Lengths:
Users with longer session lengths are more likely to convert. Provide interactive features, additional content, or personalized product suggestions to encourage extended browsing.

2. Analyze Behavior During Longer Sessions:
Understand the actions taken during extended sessions (e.g., specific pages visited or interactions) to replicate successful patterns.

3. Targeted Follow-Up:
For users with long sessions who don’t convert, use personalized follow-ups like emails or special offers to encourage purchases.

### 3. Visitor Type Strategies:

1. Boost Returning Visitor Conversions:
Returning visitors have lower conversion rates. Introduce loyalty programs, personalized recommendations, and targeted campaigns to drive repeat purchases.

2. Sustain New Visitor Conversions:
New visitors have a high conversion rate. Continue offering attractive promotions and onboarding strategies to maintain their interest.

### 4. Traffic Source Optimization:

1. Invest in High-Converting Sources:
Traffic Types 15 and 6 show high conversion rates. Increase marketing spend and refine strategies targeting these sources to maximize ROI.

2. Improve Low-Performing Traffic Sources:
Traffic Types 11 and 17 have very low engagement and conversion rates. Investigate the content, targeting, and user experience for these sources.

3. Leverage Information Pages:
Use informational pages as a funnel to guide users toward product-related pages with calls-to-action and targeted campaigns.

### 5. Region-Specific Strategies:

1. Replicate Success in High-Performing Regions:
Region 9 has the highest conversion rates. Analyze the marketing strategies and customer behavior driving this success, and replicate them in other regions.

2. Address Low-Converting Regions:
Regions with poor performance (e.g., Region 8) require a deep dive into customer needs, competitor analysis, and localized marketing strategies.

### 6. Special Day Marketing Campaigns:

1. Refine Special Day Strategies:
Current special day promotions have a negligible impact on revenue. Reassess these campaigns to ensure they resonate with the target audience.

2. Conduct Segmented Analysis:
Identify customer segments that respond differently to promotions on special days to target them more effectively.

3. A/B Test Special Day Offers:
Experiment with different promotions to identify the most impactful strategies for driving revenue during these periods.

### 7. Continuous Improvement:

1. Regular Monitoring:
Continuously monitor user behavior, page performance, and conversion rates to adapt strategies dynamically.

2. A/B Testing:
Experiment with layouts, product placements, and marketing strategies to identify what works best for various customer segments.


## Recommendations Based on the EDA & Hypothesis Testing(Campaign dataset):

### 1. Targeted Marketing Strategies Based on Education

Insight: Income levels are significantly influenced by education. Higher education levels correlate with higher incomes.

Recommendation:
Market premium and luxury products to customers with higher educational attainment.

Highlight affordable options or discounts for customers with lower educational backgrounds to increase accessibility and appeal.

### 2. Leverage Income Data for Personalized Offers

Insight: There is a strong positive correlation between income and total spending across all categories.

Recommendation:

Use income data to create personalized marketing campaigns.

Encourage higher-income customers to make premium purchases by emphasizing luxury and exclusivity in promotions.

Design value-driven offers for lower-income customers to maximize their spending potential.

### 3. Reassess Wine Marketing Strategies

Insight: There is no significant difference in wine spending between couples and individuals living alone.

Recommendation:

Shift focus from targeting based on relationship status to promoting wine as a broader lifestyle product.

Use campaigns that emphasize the experience and value of wine, appealing to all demographics regardless of marital status.

### 4. Focus Campaigns on Lower-Income Groups

Insight: Lower-income customers are more likely to accept campaigns, showing higher responsiveness to discounts and promotions.

Recommendation:

Develop campaigns tailored for price-sensitive customers, highlighting discounts, bundles, and value-for-money products.

Use simpler messaging and offers that resonate with cost-conscious shoppers.

### 5. Continuous Monitoring and Adaptation

Insight: Consumer behavior varies significantly across income and education levels.

Recommendation:

Regularly analyze and segment data to adapt marketing strategies dynamically.

Use feedback loops and periodic analysis to refine campaigns and ensure their relevance and effectiveness.
