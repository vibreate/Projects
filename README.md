# Are Private Colleges Worth the Cost?  

## Overview:


* Improved students’ college selection process by analyzing the cost-effectiveness of 800+ U.S. colleges across all 50 states using Python. 
* Demonstrated a weak positive correlation between average degree cost and average career pay with regression analysis; visualized findings using Matplotlib for the 10 highest-value schools.
* Found public schools to offer a better value as a degree costs about 35% less than one from a private school while private school graduates only earn about 5% more in terms of mid-career earning potential.

---


### Visualizations & Findings:
<br/><br/>



![](https://github.com/vibreate/Portfolio/blob/main/images/in-state%20bar%20chart.png)
<br/><br/>


![](https://github.com/vibreate/Portfolio/blob/main/images/out-of-state%20bar%20chart.png)


As shown in the 2 bar charts above, the top 3 states with the highest average tuition costs are Pennsylvania (PA), Massachusetts (MA), and New York (NY), which are all located in the East Coast.
<br/><br/>
<br/><br/>



![](https://github.com/vibreate/Portfolio/blob/main/images/top%2010%20schools.png)

The 3 best schools in terms of value are two-year degree public schools: Bellevue College, Clark College, and West Virginia University. Graduates of these schools had average salaries that are between 3 to 5 times their degree cost.
<br/><br/>
<br/><br/>



![](https://github.com/vibreate/Portfolio/blob/main/images/scatter%20plot.png)

The scatter plot shows a statistically significant correlation between total degree cost and salary potential. However, such a correlation is not strong, suggesting that the total cost of a degree is only weakly linked to future salary potential.

<br/><br/>

### Data Set Info:

* Two CSV files were used for this analysis: *salary_potential* and *tuition_cost*
* The *salary_potential* csv file details the 2018-2019 college tuition costs while the *tuition_cost* csv file contains information on early and mid-career salary potential of college graduates.
* [Data Set Source](https://www.kaggle.com/jessemostipak/college-tuition-diversity-and-pay?select=tuition_income.csv)

### Data Wrangling:

* Identifed and removed rows with missing valus in the *room_and_board* column of the *tuition_cost* csv.
* Filled missing values in the *state* column based on the corresponding values in the *state_code* column.
* Cleaned naming incosisntentcies between the *salary_potential* and *tuition_cost* csv files.
* Merged the 2 data sets into a single dataframe by left joining the *salary_potential* csv onto the *tuition_cost* csv. 
* Created new variables such as *best_value_ratio* by dividing *avg_career_pay* by *avg_degree_cost* to compare cost-effectiveness between colleges.
    - *avg_degree_cost* is obtained by taking the average of in-state and out-of state tuitions    
    - *avg_career_pay* is obtained by taking the average of early-career and mid-career pay

### Tools Used
* Python Packages Used: Pandas, NumPy, Matplotlib, Seaborn, SciPy

