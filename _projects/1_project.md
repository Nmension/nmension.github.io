---
layout: page
title: Nvidia
description: Financial Bubble Analysis – Part 1 (behind the scenes) 
img: assets/img/nvidia_bg.jpg
importance: 2
category: personal
related_publications: false
---

Here I will focus on the technical aspect such as where did I find the data, what did I use to cleanse/wrangle it, how did I generate the plots, etc and, also which difficulties/problems I met.

### **Links:**
[Github repo: technical documentation and modules](https://github.com/Nmension/Nvidia_Data_Analysis) (available)

[Analysis report](https://nmension.github.io/blog/) (not available yet)

### **Overview:** 

This project aims to assess whether the high market valuation of the company "Nvidia Inc." reflects a financial bubble by integrating structured data workflows and analytical tools.
<br /><br />

### **Setup summary:** 

#### **Data Pipeline & Storage:**

- GAAP respecting financial data collected from public company filings (10-K, quarterly reports, etc.) is stored in a PostgreSQL database called "nvidia". 
    
- A custom 500-line Bash script (manage_data.sh) was developed for non-technical users, enabling:

  - Data export guidance (via simple CLI prompts),

  - Auto-updating missing entries in the PostgreSQL DB,

  - Step-by-step data insertion support.

#### **Data Exploration & Processing:**

- The exported data (as .csv) is explored and cleansed in Jupyter Lab; using Python along with Pandas and NumPy for data wrangling and consistency checks.

#### **Visualization & Analysis:**

- A Python script generates key financial charts and tables using Matplotlib (along with the previous libraries), supporting narrative insights into revenue trends, cost structures, valuation dislocations, and systemic risk factors.

This modular setup ensures both repeatability and accessibility for collaborative, data-driven economic analysis.
<br />

### **Collection of generated plots for the first party of the project:**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/incrusted_dual_bar_plus_line_plot.png" title="Net Income YoY comparaison" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bar_line_dual_plot.png" title="Yearly Revenue per activity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The graph on the left (Figure V) shows the evolution of Nvidia's net income (year over year) compared to that of its main competitors.
    <br />
    On the right, Nvidia's revenue per activity is plotted as a bar and line graph to better illustrate the growth differential and trends between segments respectively.
</div>

The tricky part about the plots above was configuring the right parameters to get the their x and y axes synchronised.<br />

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/incrusted_double_pie_plot.png" title="Yearly Revenue per activity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This double-donut chart shows the evolution of the average revenue components between two periods: 2019-2023 and 2024-2025.
    The periods were chosen so that the difference in the impact from the AI Data Center segment on the structure is most apparent.
</div>

One difficulty I encountered with the former plot was creating a legend that has the colors of the two periods. I solved this by creating empty strings in the list of labels to avoid labels becoming redundant, while still allowing handles to appear.<br />
  Here's the code:
```python
lab = ['','','','','Net income', 'Cost of goods sold', 'Operating expenses', 'Taxes and interests']

ax.legend(lab, title='  2019-23                 2024-25', title_fontsize='small', fontsize='medium', fancybox=True, loc='lower left', bbox_to_anchor=(1, 0.1, 0.5, 1), handleheight=2, handlelength=4, ncols=2, alignment='left')
```
<br />
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stacked_bar_pie_dual_plot.png" title="Quarterly Revenue by activity segment" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Reading from the left, the first chart (II.a) shows the difference in revenue growth between the segments in their respective color each quarter, while the sum of these segments represents the quarterly total revenue.
    <br />
    The chart on the right (II.b), on the other hand, focuses on showing the significant difference in the importance of the segments to the company's total revenue (concentration risk) at the beginning of 2025. 
</div>
By pivoting the resulting dataframe from the csv formatted file, I was able to place Nvidia activity segments as rows and to separate the data by quarters per year in a double indexed fashion for columns. This transformation allowed me to to get the cumulative sums for each quarter of every year to get this bar chart. <br />

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/line_pie_dual_plot.png" title="Shareholders' groups" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure IV.a shows the evolution of three different shareholders groups while the second one (IV.b) provides an average proportion for the same period. 
</div>
The figure IV was the easiest to create because it only involved creating two plots side by side, using data operations that are natively handled in Matplotlib, without requiring a special way of organizing them or many additional steps.
<br />

### **Bash script for data management:**

If it were just for the sake of analyzing data, I wouldn't have written a bash script with so many functions, but I needed to apply what I had just learned in my recent bootcamps, and at the same time expand my knowledge as I was quickly confronted with the limits of my current programming skills. Some of the challenges I faced included finding better input validation and ways to break down SQL queries to easily guide non-technical users through indirect database queries. I also learned to use nested case statements, although I didn't want to overuse them so as not to add too much complexity to the code, although they were easier to implement. 

For more information, please check the [Github repository](https://github.com/Nmension/Nvidia_Data_Analysis) of the project.

_This page and the project it is affiliated to aren't finished yet but since I have many things to handle at the moment, I'll try my best to finish it as soon as possible. Thank you for reading !_