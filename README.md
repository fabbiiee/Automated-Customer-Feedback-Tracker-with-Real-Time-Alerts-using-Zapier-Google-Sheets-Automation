# Automated Customer Feedback Tracker with Real-Time Alerts using Zapier & Google Sheets Automation
## Overview
This project is a dynamic solution designed to streamline how customer feedback is collected, monitored, and responded to in real time. By connecting Google Forms, Google Sheets, and Zapier, the system automates feedback tracking, instantly flags negative responses, and triggers personalized email alerts for timely follow-up.
The project also features a live-updating dashboard that displays key metrics like average ratings, recommendation percentage, and feedback trends over time, empowering businesses to make informed decisions based on real customer insights without manual work.
## Data Source
The data for this project was collected through a Google Form designed to capture customer feedback after service interactions. Each response submitted through the form is automatically recorded in a connected Google Sheets spreadsheet.
The form includes fields such as:
•	Timestamp
•	Full Name
•	Email Address
•	Experience Rating (1–5 scale)
•	Feedback Description
•	Recommendation to Others (Yes/No)
This structured input provides a rich and consistent dataset, making it easy to automate tracking, analysis, and follow-up actions using Zapier.
## Tools Used
• Google Forms – For collecting structured customer feedback seamlessly.
• Google Sheets – To store and analyze response data in real time.
• Zapier – For automating workflows, including email alerts based on specific responses.
• Gmail – Used to send automated, personalized email responses based on feedback.
• OpenAI (ChatGPT) – To generate personalized email responses for negative feedback.
## Data cleaning
Minimal data cleaning was required since responses were collected directly through a structured Google Form. However, the following steps were taken to ensure the data remained analysis-ready:
•	Handled blank rows using formulas like FILTER () to exclude empty timestamps or incomplete entries.
•	Standardized date formats using ARRAYFORMULA and TEXT () to extract consistent Month-Year values for trend analysis.
•	Categorized feedback based on response to the “Would you recommend us to others?” question, which enabled filtering of negative feedback for real-time alerts.
•	Applied conditional formatting to visually highlight poor ratings and “No” recommendations in the raw response sheet for quick manual inspection.
## Analysis techniques
To derive actionable insights from the customer feedback data, the following techniques were applied:
•	Categorical Breakdown: Responses were analyzed based on key categories such as rating (1–5 stars) and recommendation status (Yes/No).
•	Trend Analysis: Monthly trends were identified by extracting and grouping responses by Month-Year, allowing us to track feedback volume and changes in customer sentiment over time.
•	Sentiment Segmentation: Using the “Would you recommend us?” field, responses were segmented into positive and negative experiences for targeted monitoring.
•	KPI Calculation: Key performance indicators such as average rating, total responses, percentage of positive recommendations, and monthly feedback trend were calculated using COUNTIF(), AVERAGE(), and ARRAYFORMULA() functions.
•	Real-Time Alert Triggering: Automation logic was set up to detect negative feedback and immediately trigger email alerts using Zapier and OpenAI-generated responses.
## Visualizations used
The dashboard was built using Google Sheets and includes the following visualizations:
•	Line Chart – Monthly Feedback Trend
Tracks the volume of feedback received each month to visualize engagement and trends over time.
•	Column Chart – Responses by Rating
Displays the number of responses per rating (1 to 5), giving a clear picture of customer satisfaction levels.
•	Pie Chart – Recommendation Breakdown
Shows the percentage of customers who would or wouldn’t recommend the service, offering a quick overview of customer loyalty.
•	Scorecards – Key Metrics
Used to display:
o	Average Rating
o	Total Number of Responses
•	Conditional Formatting – Visual Flags for “No” Recommendations
Applied in the response sheet to highlight feedback entries where customers selected “No” to recommending the service
## Key Insights
•	Overall Customer Satisfaction is Moderate to High:
The majority of responses were in the 3 to 5-star range, indicating generally satisfactory service experiences, though there is still room for improvement.
•	Notable Portion of Customers Wouldn’t Recommend:
A significant number of customers selected “No” when asked if they would recommend the service, highlighting areas of dissatisfaction that need to be addressed.
•	Common Complaints Include Delayed Response Times:
From analyzing the feedback, a recurring theme among negative responses was frustration with slow or ineffective communication.
•	Engagement Levels Fluctuate Over Time:
Monthly feedback trends show inconsistent submission rates, suggesting varying levels of customer interaction or satisfaction at different times.
•	Real-Time Alerts Enable Proactive Follow-Up:
The Zapier automation ensures that negative feedback immediately triggers an email response, allowing for faster issue resolution and improved customer relationship management.
## Challenges and learnings
1. Handling Data Insert Order in Google Sheets
One challenge was that new Google Form responses were being inserted at the top of the sheet instead of the bottom. This affected formulas and charts that were designed to update based on new entries added at the end.
Solution: Adjusted formula ranges to be dynamic and ensured proper structure in the data source to maintain accuracy.
2. Chart and Formula Dynamism
Initially, the dashboard charts weren’t updating automatically with new entries.
Learning: I refined the use of functions like ARRAYFORMULA, UNIQUE, and COUNTIF to make the dashboard truly dynamic, ensuring seamless updates without manual input.
3. Triggering Emails Only When Needed
Setting up Zapier to send personalized apology emails only when someone responded “No” to the recommendation question required careful logic and testing.
Learning: I learned how to use filters in Zapier to ensure actions only run under the right conditions, and how to troubleshoot delays in zap execution.
4. Managing Visual Clarity
With several metrics to display, keeping the dashboard clean and insightful without redundancy was a challenge.
Solution: I removed duplicate visuals (e.g., two charts showing monthly feedback counts) and replaced them with more valuable insights like “Average Rating by Month”.
## Conclusion
This project successfully demonstrates how automation and data analysis can be combined to improve customer feedback management. By integrating Google Forms, Google Sheets, and Zapier, I was able to create a streamlined system that not only collects and analyzes responses in real time, but also sends personalized follow-up emails to dissatisfied customers — helping businesses respond faster and smarter.
The dashboard offers quick, clear insights into customer satisfaction trends and overall service performance, while the automation ensures no feedback goes unnoticed.
This project highlights my ability to blend data analysis with automation tools to deliver efficient, scalable solutions that drive better decision-making




