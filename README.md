# Email-Phishing
Sample Case Study: Analyzing Phishing Emails to Enhance Staff Awareness

## Background
A mid-sized company’s IT department has observed a rise in phishing emails targeting employees. To proactively address this threat, the company aims to analyze the characteristics of phishing emails received to date. The goal is to identify patterns and risk factors, enabling the design of more effective staff awareness programs and targeted training.
## Dataset Overview
The IT department has compiled a dataset with the following fields for each email:<br>
•	num_words: Total number of words in the email body<br>
•	num_unique_words: Count of unique words used<br>
•	num_stopwords: Count of common stopwords (e.g., "the", "and", "in")<br>
•	num_links: Number of hyperlinks detected<br>
•	num_unique_domains: Number of unique domains in links (e.g., "paypal.com")<br>
•	num_email_addresses: Count of email addresses found in the text<br>
•	num_spelling_errors: Count of misspelled words<br>
•	num_urgent_keywords: Number of urgent words (e.g., "urgent", "verify", "update")<br>
•	label: Target variable (0 = Safe Email, 1 = Phishing Email)<br>
## Business Questions
•	What are the most distinguishing features of phishing emails compared to safe emails?<br>
•	Are there specific patterns (e.g., high number of links, urgent keywords) that correlate strongly with phishing attempts?<br>
•	How can these insights inform the content and focus of staff awareness programs?<br>
Key Business Metrics: False positive/negative rates if using these features for automated detection<br>

## Analysis Approach
### 1. Data Exploration (SQL & Excel)<br>
•	Use SQL to aggregate and summarize the dataset:<br>
•	Calculate the total number and percentage of true phishing emails.<br>
•	Compute average values for each feature, grouped by label.<br>
•	Identify outliers (e.g., emails with unusually high numbers of links or urgent keywords).<br>
•	Export results to Excel for further analysis and visualization.<br>
### 2. Feature Analysis (Excel)
•	Create pivot tables and charts to compare feature distributions between phishing and safe emails.<br>
•	Highlight features with the largest differences (e.g., phishing emails may have more links, spelling errors, and urgent keywords).<br>
### 3. Visualization (Tableau)
•	Build dashboards to visualize:<br>
•	The volume of phishing emails over time (identify spikes or trends).<br>
•	Feature comparison (e.g., box plots of num_links or num_urgent_keywords by label).<br>
•	Heatmaps showing the correlation between features and phishing likelihood.<br>
## Sample Insights & Recommendations
### Findings
•	Phishing emails typically contain more hyperlinks, a higher count of urgent keywords, and more spelling errors than safe emails.<br>
•	A significant spike in phishing emails was observed during certain periods (e.g., holidays or company events), aligning with findings from academic studies that attackers exploit timing and urgency24.<br>
•	Most phishing emails use ambiguous or urgent language to prompt immediate action, often without clear context24.<br>
### Actionable Recommendations
•	Awareness Training: Focus on educating staff to recognize emails with multiple links, urgent language, and poor spelling as potential phishing attempts.<br>
•	Simulated Phishing Campaigns: Use the identified high-risk features to design realistic phishing simulations for training.<br>
•	Automated Alerts: Implement rules in email filtering systems to flag emails with high counts of links, urgent keywords, or spelling errors for additional review.<br>
## Conclusion
By systematically analyzing the features of phishing emails, the company can tailor its awareness programs to address the most common tactics used by attackers. This data-driven approach ensures that staff are better equipped to identify and report suspicious emails, reducing the risk of successful phishing attacks.
