Personal Finance Power BI Dashboard

A project built using Microsoft Power BI to analyze personal financial records and transform raw expense data into interactive, insightful dashboards.

"Data analysis isn’t just about showing numbers—it’s about uncovering a story and building context from raw information. True analytics goes beyond formulas and calculations; it’s about using data to drive real, meaningful change."
— Chris Dutton, Maven Analytics

Problem Statement

For a few years, I have been tracking my day-to-day expenses in Microsoft Excel. While Excel’s sorting and filtering functions provided a basic overview, they lacked depth for advanced analysis. To gain richer insights, I decided to convert my static spreadsheets into dynamic dashboards using Power BI.

Project Objectives

The dashboards aim to answer the following questions:

What are my monthly spending trends for each year?

How much do I spend by category?

Can I view a detailed list of expenses with comments?

How much is spent across different purchase locations?

What is the distribution of purchases across price ranges?

What do my quarterly and weekly spending patterns look like?

What are my average daily, weekly, and monthly expenses?

How do food costs compare with restaurant costs?

How does my spending change when I’m sick?

How does weekend spending differ from weekdays?

Before building visuals, I mapped out the required measures and drafted a rough dashboard layout.

Analysis Summary

I developed multiple dashboards to explore these questions. Sample views:




Tools & Technologies

Python (v3.8)

Python libraries: openpyxl, os

Windows 10

Microsoft Power BI Desktop (v2.93)

Microsoft Excel

Apple iPad (7th Gen) + Pencil

About Microsoft Power BI

Power BI is Microsoft’s business intelligence platform that enables data import, modeling, and visualization. First launched in 2011, it has steadily evolved with new features added monthly. It can be used both locally via Power BI Desktop or online through Power BI Service. While somewhat similar to Excel, Power BI makes it much easier to create interactive and visually engaging dashboards.

Repository Structure
Finance_Data/20xx

Contains monthly Excel files of expenses, covering Aug 2018 – Dec 2020.

change_excel_sheets.py

Python script that renames multiple Excel sheet tabs to “Sheet1” for smoother Power BI integration.

Finance_Data.xlsx

The original Excel workbook where I tracked spending.

Personal_Finance_Dashboard.pbix

The Power BI file containing all dashboards and visuals.

Data Collection

I manually entered expense data into Excel using purchase receipts. The dataset includes Date, Category, Price, Location, and Comment.

Because my data was spread across multiple sheets within a workbook, I split them into individual Excel files to simplify Power BI imports.

Data Cleaning

Several preprocessing steps were required:

Category standardization: Fixed inconsistent category labels (e.g., “hair cut”, “Hair-Cut” → “Hair Cut”).

Date formatting: Standardized mixed formats (Text, General, Date).

Null values: Removed rows with missing values, since they were minimal and did not affect results.

Measures & Visuals

To answer the research questions, I created three lookup tables:

Calendar Lookup – Generated date ranges with derived fields such as month, quarter, week-ending, etc.

Item Lookup – Contained unique categories; included a Boolean column to toggle rent on/off for analysis.

Location Lookup – Unique purchase locations.

Using these, I built measures such as:

Total cost

Average daily/weekly/monthly cost

Purchase counts by price range

Flags for sick days, weekday/weekend spending

Key visuals include slicers for date, category, location, health status, weekday/weekend, and price ranges—offering flexible granularity.

Conclusion

By leveraging Power BI, I transformed static expense logs into interactive dashboards, providing deeper insights into personal spending habits. These dashboards make it easier to identify trends, compare categories, and make informed financial choices.

Try It Yourself

Download Power BI Desktop
👉 https://powerbi.microsoft.com/en-us/desktop/

Adjust Settings

File → Options → Preview Features: uncheck all

File → Options → Data Load: disable relationship auto-detection

File → Options → Regional Settings: adjust to your region

Open the Project
Download this repo, open the .pbix file in Power BI Desktop, and start exploring the dashboards.

Future Enhancements

Improve dashboard design with professional templates.

Develop a generalized version for anyone to use (possibly via Docker).

Introduce new metrics and comparisons.

Optimize dashboards for mobile and tablet viewing.



Acknowledgements

Microsoft’s Power BI team for a powerful analytics tool.

Cashiers who helped by printing receipts.

Everyone visiting and exploring this project!
