---
layout: post
title: Nvidia Analytical Report
date: 2025-06-27 11:12:00-0400
description: multidimensional analysis
tags: analysis
categories: economics finance
related_posts: false
---

# **Economic & Financial Report: NVIDIA Corp.**  
### *Is Nvidia the leader of a Revolution or a Financial Bubble ?*

## **Main report objective**

This report evaluates whether the high valuation of Nvidia represents a financial bubble.
Using public financial data and a data-driven approach, I analyze both **micro** and **macro** dimensions to find the answer.  

The analysis draws on revenue trends, efficiency ratios, balance sheet health, and systemic risk exposure to conclude that **Nvidia’s valuation may or may not be supported by fundamentals**, placing it at **risk of being within a financial bubble**.

---

## **Table Of Contents**

**I. Business Growth**  
**II. Efficiency**  
**III. Valuation vs Fundamentals**  
**IV. Balance Sheet Fragility**  
**V. Macro Positioning**  
**VI. Risks & Stylized Valuation Scenarios (2025–2030)** 

---
### **I. Business Growth**  
##### **I.a. Revenue Compound Annual Growth Rate between 2019 & 2025**
  - Formula used for this section:


$$
CAGR = \left(\frac{Ending\ Value}{Starting\ Value}\right)^\left.\frac{1}{t}\right. - 1 * 100
$$


The corporation's revenue CAGR between 2019 and 2025 is **41.11 %**. As is, it reveals a very strong growth over a period of 7 years. For comparison, for the same period, it is almost _2.5 times that of Nasdaq-100_ and only _10 points lower than Bitcoin's_. 



The only problem with this metric is that it doesn't tell us more than that, so we need to look more specifically into Nvidia's balance sheets to see if this CAGR is stable throughout the period or if only a part of it is responsible for its elevated value.

  - The following plot (**I**) does just that by showing how overall and segment-specific revenues evolved every year.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bar_line_dual_plot.png" title="Yearly Revenue per activity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


We can see from this plot that the high revenue CAGR originates from the end of the period, more accurately in 2024 and 2025, thus positively biasing its value. 

On the subplot on the right, we can see that there is a strong correlation between the total revenue variations and its respective top two segments. <br \>
In 2023, the same relationship shifts between the whole and a unique segment only, implying a stronger concentration risk. 


##### **I.b. Segment concentration risk:**


Though we can already tell from the plot in the previous section which of Nvidia's segments is the most important, we will specifically look closer by using quarterly revenue data per segment. This is also to get a more accurate understanding of the hinted existing concentration risk.


Therefore, the next formula was carefully selected to verify the ratio of revenue contribution per segment.


$$
Segment\ Contribution\ Ratio = \frac{Revenue\ per\ Segment}{Total\ Revenue}
$$

Using SCR's formula, I generated the next plot on the left, also making trend and pattern recognition more practical.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stacked_bar_pie_dual_plot.png" title="Quarterly Revenue by activity segment" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Plot II-a shows that Gaming (yellow colored) has been the most stable segment, sustaining Nvidia's revenue, as it is the one that has the lowest variance across quarters while being a significant part of it.  <br />
Until the second quarter of 2024, the second most important segment of the company was the **Data Center** one before it later reached first place as their GPUs took a strategic position in the Artificial Intelligence sector.  <br />
In 2025, from plot II-b, we see that 88.3% of their total revenue is dependent on this latest green colored segment, while Gaming now only accounts for 8.7% of it.

That's why we can affirm that today's revenue of Nvidia is highly concentrated and dependent on the AI sector's evolution.



### **II. Efficiency**
This section evaluates how effectively Nvidia converts its revenue into operating profit and identifies where operational pressure or inefficiency may lie. In addition to traditional profitability ratios, we examine cost structure dynamics over time.

##### **II.a. Traditional profitability ratios:**
The first formula of this subsection will help us measure how efficiently Nvidia turns revenue increases into operating income.

$$
Operating\ Leverage\ Ratio = \frac{\text{Δ Operating Income %}}{\text{Δ Revenue %}} 
$$


The next one captures profitability before interest and taxes.


$$
Operating\ Margin = \frac{\text{Operating Income}}{\text{Revenue}} 
$$


Using both of the previous formulas, we get the following table for the studied period.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nvidia_table_1_efficiency.png" title="table 1: Profitability" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Though Nvidia's operating margins mainly increased during our selected timeline, nearly doubling, this is mostly due to increasing total revenue more than decreasing operating expenses.


The operating leverage ratio confirms that assumption as,for four years out of six, it is above one, showing that Nvidia's profitability is very dependent on their sales. A small increase in revenue can lead to a bigger increase in profits but the opposite is also true, as seen for 2020 and 2023. _It is advantageous in periods of increased sales_ but at the same time, _risky in times of decreases_ as the fixed costs still have to be accounted for no matter what the sales are._


In other words, the higher leverage reveals that the company has high fixed costs, thus elevated operating expenses, and that their break-even point for sales is dependent on covering these ones but also a part of why they became the dominant company in the AI GPU data center as they had the required assets and strategy, available at the right time.




##### **II.b. Cost structure dynamics over time:**

At this point, we want to take a closer look at the different components of the company's revenue to get a better picture of its internal efficiency. 


For all reasons found in prior sections, I carefully selected two periods to compare, for this plot, that also aligns with the idea of revenue concentration risk in one segment. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/incrusted_double_pie_plot.png" title="Evolution of the average revenue structure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


From the revenue structure of the two periods, we see that net income has substantially increased, from 27.2 % on average between 2019 & 2023 to 45.0 % in 2024-2025, or a positive difference of 17.8 points between periods. <br />
This is explained by the improvement of the internal cost components of the revenue, though the external ones deteriorated (Taxes and interests): COGS went from 38.7 % to 30.0 % (an -8.7 points difference), and OpEx went from 34.0 % to 20.9 % (-13.1 points) while Taxes and interests rose from less than 0.1 % to 4.2 % (+4.1 points); we get: 17.8 % =~ 8.7 + 13.1 - 4.1


Though these results could be seen as promising, we have to keep in mind that they are about percentages and therefore incomplete to solely interpret by themselves. If we keep in mind the growth difference in revenue and compare it to the improvement of the cost structure for the same periods, the latter loses a part of its appeal, though we can affirm that Nvidia is still more efficient nowadays than in the past.  


### **III. Valuation vs Fundamentals**  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nvidia_table_2_valuations.png" title="table 2: Valuations Vs Fundamentals" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


What we see from the table above is that before the boom of the Data center AI segment of the company (2023 and prior), for three out of four years, EV and market cap both skyrocketed while net income lagged behind. This is a potential bubble indicator, as it signals that market expectations were decoupled from reality, suggesting some type of investor exuberance at the time. <br />
However, in 2024, the situation got inverted as EV and MC growth percentages were 3 times lower than the net income's.


### **IV. Balance Sheet Fragility**  


### **V. Macro Positioning**  


### **VI. Risks & Stylized Valuation Scenarios (2025–2030)**