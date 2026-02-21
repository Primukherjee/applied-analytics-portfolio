# Strategic Portfolio Fragility & Market Power Modeling in Multi-SKU E-Commerce

## Executive Summary

This project models structural revenue concentration in a multi-category e-commerce business using HHI and dynamic stress simulation. 

Although baseline concentration appears low (HHI = 0.05), stress testing reveals nonlinear fragility, where category shocks increase concentration and expose structural dependency.

The analysis demonstrates how surface diversification can mask systemic vulnerability.

## What I’m Curious About

In this project, I am exploring structural dependency inside a multi-category e-commerce business.

I wanted to understand:

- Is revenue structurally concentrated across product categories?
- Are a few categories carrying most of the business?
- Is portfolio diversification real, or is it an illusion?
- What happens to total revenue and market concentration if one dominant category is shocked?
- Does concentration increase under stress?

This project shifts from customer dependency (Project 2) toward structural product-level fragility.

---

## Why This Matters to Me

In psychology, we often examine patterns of dependency — where systems appear stable but are structurally leaning on a small set of supports.

Businesses are not very different.

If revenue is driven disproportionately by one category, the system may appear diversified while actually being exposed.

This project treats the product portfolio as a structural system and tests its resilience under simulated stress.

---

## The Data

I used the Brazilian Olist e-commerce dataset from Kaggle, specifically:

- olist_orders_dataset
- olist_order_items_dataset
- olist_products_dataset
- product_category_name_translation

The dataset includes:

- Product IDs
- Category mappings
- Order timestamps
- Revenue per order item
- Unit pricing
- Seller information

The analysis is illustrative rather than definitive, focusing on structural revenue patterns rather than causal claims.

---

## How I Approached the Analysis

I built the entire project in Power BI using DAX-based modeling.

The analysis is divided into three structural layers:

1. Market & Revenue Structure  
2. Cannibalization Diagnostics  
3. Strategic Stress Simulation  

---

# Page 1: Market & Revenue Structure

This section establishes the structural baseline.

### Revenue Distribution by Category

The largest category:

- health_beauty generated approximately 1.44M in revenue.

There is a clear steep drop-off after the top categories, showing uneven distribution across product categories.

This immediately suggests concentration rather than diversification.

---

### Herfindahl–Hirschman Index (HHI)

HHI = 0.05

In economic terms:

- Below 0.15 → unconcentrated
- 0.15–0.25 → moderate concentration
- Above 0.25 → high concentration

At 0.05, the portfolio appears diversified at a high-level category view.

However, this is only the surface layer.

## Mathematical Formulation of HHI
HHI = Σ (Revenue Share_i²) 

### Revenue & Units Growth

Year-over-Year Metrics:

- Revenue YoY Growth ≈ 1.22
- Units YoY Growth ≈ 1.21
- Price YoY ≈ 0.00

This suggests growth is volume-driven rather than pricing-driven.

---

### SKU-Level Concentration

Top individual SKUs contribute approximately:

- 0.43%
- 0.38%
- 0.37%

This indicates that while category-level concentration is low, SKU-level fragmentation is high.

---

### Portfolio Fragility Index

Portfolio Fragility Index = 0.30

This metric reflects sensitivity of total revenue to top contributor segments.

Even if high-level HHI appears low, fragility can still exist when dominance emerges inside subsets.

---

# Page 2: Cannibalization Diagnostics

Here, I examined whether categories are shifting share over time.

### Category Share Trends

Top 5 categories show:

- Share shifts between 2016 → 2017 → 2018
- Certain categories gained share while others declined

Most share changes were small (±0.01), suggesting relative stability at category level.

However, small shifts in dominant categories can still produce meaningful structural changes.

---

# Page 3: Strategic Stress Simulation

This is the core modeling section.

I simulated a revenue shock applied to the largest category (health_beauty).

Using a dynamic slider parameter (Category Shock %), I applied stress from 0% to 50%.

---

## Baseline Revenue

Base Revenue ≈ 16M

---

## Stressed Revenue

At 50% shock:

Stressed Revenue ≈ 15.12M

Revenue Impact ≈ -5%

Even removing half the revenue from the largest category reduces total revenue by 5%.

---

## HHI Under Stress

Baseline HHI = 0.05

At 50% shock:
HHI = 0.12

Concentration Increase = +0.07

When the dominant category weakens, concentration increases.

Other categories absorb relative share, increasing structural dependency.

---

## Structural Interpretation

From 0% to 30% shock:

HHI remains relatively stable.

After ~30% shock:

HHI increases more rapidly.

This suggests nonlinear fragility.

The system appears stable until stress crosses a threshold.

---

## Limitations

- The dataset is observational and illustrative.
- No causal inference.
- Category-level aggregation may hide SKU-level dependencies.
- Time range limited to available years.

---

## Tools Used

- Power BI
- DAX (dynamic measures & simulation)
- Parameter-driven stress modeling
- HHI computation
- Share-based concentration metrics

---

## Overall Interpretation

Even when concentration metrics appear low, fragility can exist under stress.

Stability in business systems is often conditional — not absolute.

Portfolio structure matters more than surface diversification.

---

## What Businesses Should Focus On

- Monitor HHI under simulated stress, not just static HHI
- Track share shifts across top categories quarterly
- Build diversification across mid-tier categories
- Identify nonlinear thresholds where fragility accelerates
- Stress-test portfolio concentration routinely

