# The Analysis

## 1. what are the most demanded skills for the top 3 most popular data roles?

I filtered out those positons by which ones were the most popular, and got the top 5 skills for these top 3 roles
"Lorem ipsum" is a nonsensical, jumbled Latin-like placeholder text used in graphic design, publishing, and web development to demonstrate typography and layout without being distracted by meaningful content. It is derived from a 45 B.C. Latin text by Cicero, with words altered and removed to make it meaningless. The first two words, "lorem ipsum," come from a truncated version of the phrase "dolorem ipsum," meaning "pain itself".

View my notebook with detailed step hear :[Click here](2_skills_count.ipynb)


### Visualize Data

```python 
fig, ax = plt.subplots(len(job_titles), 1)


for i, job_title in enumerate(job_titles):
    df_plot = df_skills_perc[df_skills_perc['job_title_short'] == job_title].head()
    sns.barplot(data=df_plot, x='skll_percent', y='job_skills', ax=ax[i], hue='skill_count', palette='dark:b_r')

plt.show()
```

### Results
![Skill Demand Percent](images\skill_demand_percent.png)


### Insights
"Lorem ipsum" is a nonsensical, jumbled Latin-like placeholder text used in graphic design, publishing, and web development to demonstrate typography and layout without being distracted by meaningful content. It is derived from a 45 B.C. Latin text by Cicero, with words altered and removed to make it meaningless. The first two words, "lorem ipsum," come from a truncated version of the phrase "dolorem ipsum," meaning "pain itself".
##
## 3. How well do jobs and skills pay for Data Analysts

### Salary analysis for Data Nerds
#### Visualize Data
```python
sns.boxplot(data=df_US_top6, x='salary_year_avg', y='job_title_short', order=job_order)
sns.set_theme(style='ticks')

ticks_x = plt.FuncFormatter(lambda y, pos: f'${int(y/1000)}k')
plt.gca().xaxis.set_major_formatter(ticks_x)
plt.show()
```
![Salary Distribution of Data Jobs in the US](images\output.png)
*Box plot Visualizing the salary distribution for the to 6 data job titles.*

### Insights
"Lorem ipsum" is a nonsensical, jumbled Latin-like placeholder text used in graphic design, publishing, and web development to demonstrate typography and layout without being distracted by meaningful content. It is derived from a 45 B.C. Latin text by Cicero, with words altered and removed to make it meaningless. The first two words, "lorem ipsum," come from a truncated version of the phrase "dolorem ipsum," meaning "pain itself".


