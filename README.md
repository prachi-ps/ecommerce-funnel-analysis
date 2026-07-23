# 🛒 E-commerce Funnel Analysis (SQL / BigQuery)

## Overview
This project analyzes user behavior through an ecommerce sales funnel using SQL in Google BigQuery. It tracks how users move from viewing a product to completing a purchase, identifies where users drop off, and evaluates which traffic sources drive the most engagement.

## Dataset
**Table:** `user_events`

| Column         | Description                                  |
|----------------|-----------------------------------------------|
| event_id       | Unique identifier for each event              |
| user_id        | Unique identifier for each user               |
| event_type     | Stage of the funnel (view, cart, checkout, payment, purchase) |
| event_date     | Date the event occurred                       |
| product_id     | Product associated with the event             |
| amount         | Transaction amount (where applicable)         |
| traffic_source | Channel that brought the user (e.g. organic, paid, email, social) |

## What This Project Covers
- **Funnel definition**: Structured user events into funnel stages: views -> cart -> checkout -> payment -> purchase
- **Conversion rate analysis**: Calculated conversion rates between each stage to identify where users drop off
- **Traffic source analysis**: Identified which traffic sources contributed the most users and conversions

## Tools Used
- Google BigQuery
- SQL (CTEs, aggregations, conditional counting)

## File
- `query.sql`: main query covering funnel staging, conversion rates, and traffic source breakdown

## Key Findings
- **Organic traffic** drove the highest volume of visits, making it the top acquisition channel by traffic count.
- **Email traffic**, however, had the highest conversion ratec showing that while organic brings the most users in, email brings the most qualified/ready-to-buy users.
- **View -> Cart** conversion was the drop-off point in the funnel at just **31%**, suggesting most users who view a product don't add it to their cart.
- **Payment -> Purchase** had the strongest conversion rate at **92%**, meaning once a user reaches payment, they almost always complete the purchase, the funnel's weak point is earlier, not at checkout.

## Key Takeaway
This project demonstrates the ability to translate raw event-level data into a structured funnel analysis, a common real-world use case for ecommerce and product analytics teams.
