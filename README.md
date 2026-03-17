# hotel-cancellation-analysis
# Predicting Hotel Cancellations: A Data-Driven Approach to Revenue Protection

**One-line hook:** Using machine learning to identify which bookings are likely to cancel — before it's too late to do anything about it.

---

## The Business Problem

A Portuguese hotel chain is losing significant revenue to booking cancellations, with over 1 in 3 reservations never resulting in a stay. The problem isn't just lost income — it's the missed opportunity to resell those rooms in time. Without a way to predict which bookings are at risk, the hotel is essentially flying blind until the cancellation hits.

## The Data

We analyzed over 119,000 individual bookings from two Portuguese hotels spanning 2015 to 2017, sourced from a publicly available hospitality dataset. Each record captures everything from how far in advance the guest booked to what channel they used, whether they made special requests, and their history of past cancellations. The target variable — whether the booking was ultimately cancelled — already sits at 37%, making this a meaningful and actionable prediction problem.

## Key Discoveries

- **Book early, cancel often:** Guests who cancelled booked an average of **170 days** in advance, compared to just 80 days for guests who showed up. The further out the booking, the higher the risk.
- **OTA bookings are a liability:** Reservations made through Online Travel Agencies cancelled over **50% of the time**, while direct bookings cancelled at just 15% — making the booking channel one of the strongest cancellation signals in the data.
- **Special requests signal commitment:** Guests who made 3 or more special requests cancelled less than **10% of the time**. Engaged guests are reliable guests.
- **Loyalty is a cancellation hedge:** Repeat guests cancelled at just **14%** compared to 37% for first-timers, suggesting that loyalty programs do more than drive revenue — they stabilize it.

## Visualizing the Story

![Cancellation Rate by Market Segment](market_segment_cancellation.png)

*OTA bookings cancel at more than 3x the rate of direct bookings — shifting even a fraction of reservations to direct channels could meaningfully reduce the hotel's cancellation exposure.*

## Prediction Model

Using a Gaussian Naive Bayes classifier trained on booking behavior and channel data, our model correctly predicts cancellation outcomes **80% of the time**. In practical terms, for a hotel processing 1,000 bookings a month, that means catching roughly **74 cancellations early** — enough lead time to resell rooms, adjust staffing, or reach out with a retention offer before the revenue walks out the door.

## Recommendations

1. **Automate outreach for long lead-time bookings:** Bookings made 200+ days out cancel at nearly double the rate of short-lead reservations. A simple automated re-confirmation email at the 30-day mark could recover an estimated 15–20% of those at-risk bookings.
2. **Incentivize direct bookings over OTA:** OTA guests cancel at 50%+ while direct guests cancel at 15%. Offering a small perk — free breakfast, early check-in — for booking direct could shift the mix and cut the overall cancellation rate meaningfully.
3. **Build a first-stay loyalty conversion strategy:** Repeat guests are 2.6x less likely to cancel than first-timers. Targeting first-time guests with a post-stay offer to return would compound cancellation reduction over time while lowering acquisition costs.

## Tools & Techniques

Python | Pandas | Scikit-Learn | Matplotlib | Seaborn | Gaussian Naive Bayes | Google Colab

---

*This project was completed as part of ISOM 835: Predictive Analytics at Suffolk University's Sawyer Business School.*
