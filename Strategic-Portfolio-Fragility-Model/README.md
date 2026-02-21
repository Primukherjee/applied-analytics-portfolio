# Strategic Portfolio Fragility and Market Power Modeling in Multi-SKU E-Commerce Data

## Executive Summary
In this project, I am using a multi-category e-commerce business to model structural revenue concentration by incorporating HHI and a stress simulation. I found the baseline HHI to be low (0.05), but then after stress testing, I found that shocks in the categories leads to nonlinear fragility and an increase in concentration and exposes structural dependency. This project shows how exactly vulnerabilities can be easily masked by surface-level diversification. 

## What I’m Curious About
I want to understand a few things:
- Across product categories, is the revenue concentrated structurally? 
- Is the business being carried by only a few categories?
- Is portfolio diversification real?
- If there is shock in one dominant category, what happens to total revenue and market concentration?
- Does concentration increase under stress?
In this project, there's a shift from customer dependency (Project 2) to fragility at the product-level.

## Why This Matters to Me
The system as a whole might appear to be diversified when being exposed if revenue is is only driven by one category significantly. So this project is treating the product portfolio as purely structural and also testing resilience under stressful conditions. 

## The Data
In this project, I am using the Brazilian Olist e-commerce dataset from Kaggle but only these specific datasets:
- olist_orders_dataset
- olist_order_items_dataset
- olist_products_dataset
- product_category_name_translation
These datasets include:
- Product IDs
- Category details
- Order timestamps
- Revenue per order item
- Unit pricing
- Seller information
Also, this analysis is purely illustrative and should not be used to generate causal claims.

## How I Approached the Analysis
I am approaching this project using Power BI and using DAX-based modeling. I divided the analysis into three layers: 
1. Market & Revenue Structure  
2. Cannibalization Diagnostics  
3. Strategic Stress Simulation  

# Page 1: Market & Revenue Structure

### Revenue Distribution by Category
In this section, the largest category found was:
- health_beauty generated approximately 1.44M in revenue.
I also observed that there was a steep drop-off after top categories that shows that there is uneven distribution across the product categories. This suggests that there is concentration instead of diversification. 

### Herfindahl–Hirschman Index (HHI)
The HHI was found to be = 0.05 which economically would mean:
- Below 0.15 is unconcentrated
- 0.15–0.25 is moderately concentrated
- Above 0.25 is highly concentrated
The portfolio appears to be diversified at a high level category view since HHI is so small. Again, this is only surface layer.

## Mathematical Formulation of HHI
I used this calculation: HHI = Σ (Revenue Share_i²) 

### Revenue & Units Growth
Year-over-Year Metrics show in the analysis:
- Revenue YoY Growth ≈ 1.22
- Units YoY Growth ≈ 1.21
- Price YoY ≈ 0.00
This all suggested that growth is not price-driven but actually volume driven. 

### SKU-Level Concentration
In this part of the analysis, contributions made by top individual Stock keeping units were: 
- 0.43%
- 0.38%
- 0.37%
This suggest that even though concentration across the category level is low, fragmentation at the SKU level is high.

### Portfolio Fragility Index
I found the portfolio Fragility Index to be 0.30. This means that total revene is sensitive and influenced by top contributors. So this means that even though HHI is appearing to be considerably low, fragility can still exist in the system as soon as there is emergence of dominance.

# Page 2: Cannibalization Diagnostics
In this page of the analysis, I examined if there is shift in the categories over a timely manner. 

### Category Share Trends
In this, the top 5 categories show that: 
- Share shifts between 2016 to 2017 to 2018.
- Certain categories gained share while others declined.
Majority share changes were small (±0.01) that suggests that at the category-level, there is relative stability. But in spitie of this, structural changes can still occur if there are small shifts in the dominant categories. 

# Page 3: Strategic Stress Simulation
This section is the main place where I incorporated modeling, where I applied a simulated shock (revenue) to the largest category that was health_beauty. I used a slider parameter (Category Shock %), where I also applied stress from 0% to 50%.

## Baseline Revenue
The baseline revenue came out to be as 16M. 

## Stressed Revenue
At 50% shock:
Stressed Revenue ≈ 15.12M
Revenue Impact ≈ -5%
This means that total revenue would reduce by 5% if even half of the revenue was removed from the largest category.

## HHI Under Stress
Since Baseline HHI = 0.05 and at 50% shock: HHI = 0.12, there is an increase in concentration by +0.07. So we see that concentration increased when dominant category was weakened whereas for other categories, dependency increases when relative share is absorbed by the rest of the categories. 

## Interpretation
From 0% to 30% shock: HHI remains relatively stable but after ~30% shock: HHI increases more rapidly suggesting nonlinear fragility. 

## Limitations
- The dataset is illustrative and observational.
- No causal claims can be made.
- SKU-level dependencies might be hid by category-level aggregations.
- Time range is only limited to the years that are available.

## Tools Used
- Power BI and DAX (dynamic measures & simulation)
- Parameter-driven stress modeling
- HHI computation

## Overall Interpretation
In conclusion, fragility might still exist under stressful conditions in spite of concentration metrics might be to the lower side. So this leads me to say that in businesses, stability is not always absolute but can be conditional and what matters more than surface level diversification is portfolio structure. 

## What Businesses Should Focus On Based on This:
- The business should monitor HHI under stressful conditions under simulations.
- It should also track share shifts across top categories on a quarterly basis.
- It shoudl build diversification across more mid-tier categories.
- The business should stress-test portfolio concentration routinely.

## Dashboard Preview
- Market Structure (screenshots/page1_structure.png)
- Cannibalization Diagnostics (screenshots/page2_cannibalization.png)
- Strategic Stress Simulation (screenshots/page3_stress_simulation.png)
