# Comparitive-Analysis-of-Inc.-Companies-using-Power-BI


### Aim: To perform a comparative analysis of different Inc. companies with the help of Power BI.

### About the Data set: 
The data set (Inc 5000 Companies_Dataset) contains informations of 5000 inc. companies and contains features like rank, profile, name, url, state, revenue,etc.

### Project Details:

While doing this project the first thing that came to my mind is, what is an inc. company? The amswer to this question is as following:

The word "incorporated" indicates that a business entity is a corporation. ... "Inc." is an abbreviation of "incorporated," and both the abbreviation and the full word mean that a company's business structure is a legal corporation. A corporation or "Inc." is an entirely separate entity from its owners and shareholders.

The second question that came to my mind is, why do companies use inc.?

Incorporated means that a business has filed documents with a state to become a corporation. The term incorporated is used because, by filing the certificate of incorporation and going on record with the state, the owners become legally separate from their investment and the business itself.

The following are the project steps that I did to perform a comparitive analysis of inc. companies:

1. A duplicate of the Revenue column was made using the duplicate column option inside Add Column in the Power Query Editor and named as revenue_New.

2. The revenue_New column was splitted using the split by delimiter function inside the Transform tab in the Power Query Editor. The Number were
seperated from the millions or billions units by stting delimiter as space. revenue_New.1 was the column name containg the number and 
revenue_New.2 was the column containing the Million or Billion unit.

3. A new custom column (Rev_value) was added that will replace the Million with 1000000 and the Billion with 1000000000.

```=if [revenue _New.2]="Million" then 1000000 else 1000000000```

4.  Another custom column was made named Rev_final by multiplying the revenue_New.1 with Rev_value to get the exact revenue in
millions or billions. Datatype was changed to decimals.

``` =[revenue _New.1]*[Rev_value]```

5.  Area chart was plotted with industry as axis and values as Rev_final. From this chart, we can see that Health industry generates the
highest revenue compared to other industries.

6. Tree map showing the names of the top 10 companies in terms of Rev_final was made.

7. A table showing the city wise company count was made and sorted in descending order with respect to count of company names.

8. Finally, a table showing name, industry, founded, city, workers, Rev_final, growth% were displayed to give an overall
insight. Web Url's of respective companies were also added.

### Installation:

The following steps will guide you to install Power BI Desktop and run the project at your local machine:

1. Download and install Power Bi Desktop from [here](https://www.microsoft.com/en-in/p/power-bi-desktop/9ntxr16hnw1t#activetab=pivot:overviewtab).
2. Clone this github repository or download as zip.
3. Once Everything is done, open the .pbix file. 

If you already have Power BI Desktop, then you can skip the first step.

### A Glimpse of the Dashboard:

![Screenshot (176)](https://user-images.githubusercontent.com/75041273/133970780-226a7d2b-3ccb-4625-b293-bc20b36ffb1e.png)

### Tech Stack:

<img src="https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black"/> 

