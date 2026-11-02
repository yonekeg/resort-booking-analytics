# Resort Bookings Data Dictionary

`resort_bookings.csv` contains 1,400 simulated resort bookings. One row is one booking. All predictors were available when the booking arrived; the two outcomes were recorded later. The data are fictional and do not represent real guests or resort performance. Generate the file with `Rscript dev_scripts/generate_homework_case_data.R` from the repository root.

| Variable | Meaning |
|---|---|
| `booking_id` | Anonymous booking identifier; exclude from modeling. |
| `booking_lead_days` | Days between booking and planned arrival. |
| `nights` | Booked nights. |
| `party_size` | Number of guests on the booking. |
| `booking_channel` | Direct, travel agent, or online agency. |
| `loyalty_tier` | Tier known at booking. |
| `trip_type` | Leisure, business, or conference. |
| `weekend_arrival` | 1 if arrival is on a weekend, 0 otherwise. |
| `prior_stays` | Number of earlier stays. |
| `quoted_room_rate_usd` | Nightly rate quoted at booking, in US dollars. |
| `total_stay_spend_usd` | Total realized spend for the stay, in US dollars. Recorded after checkout. |
| `returned_within_year` | 1 if the guest returned within a year, 0 otherwise. Recorded later. |

The generated relationships are mostly additive for spending and probabilistic for return behavior. Neither outcome should be used as a predictor of the other.
