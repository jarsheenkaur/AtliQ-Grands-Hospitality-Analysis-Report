# AtliQ Grands Hospitality Analysis Report [Power BI]
Developed an extensive Power BI Dashboard for Revenue Management team of AtliQ Grands utilizing Power Query for data transformation, DAX for custom measures, and a variety of Power BI visualizations for effective data representation. The dashboard offers a comprehensive overview of key performance metrics, revenue sources, booking trends, and property-specific insights. Interactive features like data filters and page navigation facilitate easy exploration of data subsets, enabling AtliQ Grands to optimize pricing, enhance marketing strategies, and improve operational efficiency to regain market share and revenue in the luxury/business hotels segment.

## Problem Statement

**Provide Insights to the Revenue Team in the Hospitality Domain**

**Domain:**  Hospitality       **Function:** Revenue

AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue. However, they do not have an in-house data analytics team to provide them with these insights.
Their revenue management team had decided to hire a 3rd party service provider to provide them with insights from their historical data.

## About Data

The data as well as the problem statement are part of Codebasics Resume Challenge #1 (https://codebasics.io/challenge/codebasics-resume-project-challenge). It consists of the following 5 Tables (as CSV files) :-

Table dim_date contain 4 columns and 92 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| date                | This column represents the dates present in May, June, and July.                                                                                    |
| mmm yy              | This column represents the date in the format of mmm yy (monthname year).                                                                           |
| week no             | This column represents the unique week number for that particular date.                                                                             |
| day_type            | This column represents whether the given day is Weekend or Weekday.                                                                                |

Table dim_hotels contain 4 columns and 25 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                        |
| property_name       | This column represents the name of each hotel.                                                                                                      |
| category            | This column determines which class[Luxury, Business] a particular hotel/property belongs to.                                                       | 
| city                | This column represents where the particular hotel/property resides in.                                                                              |

Table dim_rooms contain 2 columns and 4 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| room_id             | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| room_class          | This column represents to which class[Standard, Elite, Premium, Presidential] particular room type belongs.                                         |

Table fact_aggregated_bookings contain 5 columns and 9,200 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                        |
| check_in_date       | This column represents all the check_in_dates of the customers.                                                                                     |
| room_category       | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| successful_bookings | This column represents all the successful room bookings that happen for a particular room type in that hotel on that particular date.               |
| capacity            | This column represents the maximum count of rooms available for a particular room type in that hotel on that particular date.                       |


Table fact_bookings contain 12 columns and 134,590 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| booking_id          | This column represents the Unique Booking ID for each customer when they booked their rooms.                                                       | 
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                       | 
| booking_date        | This column represents the date on which the customer booked their rooms.                                                                          | 
| check_in_date       | This column represents the date on which the customer check-in(entered) at the hotel.                                                               |
| check_out_date      | This column represents the date on which the customer check-out(left) of the hotel.                                                                 |
| no_guests           | This column represents the number of guests who stayed in a particular room in that hotel.                                                          |
| room_category       | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| booking_platform    | This column represents in which way the customer booked his room.                                                                                  | 
| ratings_given       | This column represents the ratings given by the customer for hotel services.                                                                       | 
| booking_status      |  This column represents whether the customer cancelled his booking [Cancelled], successfully stayed in the hotel [Checked Out] or booked his room but not stayed in the hotel [No show].                                                                                                                                     | 
| revenue_generated   | This column represents the amount of money generated by the hotel from a particular customer.                                                       |
| revenue_realized:   | This column represents the final amount of money that goes to the hotel based on booking status. If the booking status is cancelled, then 40% of the revenue generated is deducted and the remaining is refunded to the customer. If the booking status is Checked Out/No show, then full revenue generated will goes to hotels. |

## Dashboard Features

- 4 Different Dashboards for Quick Insights
- Multiple Data Filters
- Navigation Pane
- Monthly and Weekly Trends for Key Metrices
- Revenue, Booking and Property Analysis done on basis of Various Parameters.
- Drill Down available for Booking % and Revenue Contribution %.

## List of KPIs Created

- ABW (Average Booking Window)
- ADR (Average Daily Rate)
- ALOS (Average Length of Stay)
- Average Rating
- Cancellation %
- DBRN (Daily Booked Room Nights)
- DSRN (Daily Sellable Room Nights)
- DURN (Daily Utilized Room Nights)
- Occupancy %
- Realisation %
- Revenue
- RevPAR (Revenue Per Available Room)
- Total Bookings
- Total Capacity

## Screenshots

![PSS (1)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/560b9907-9d53-4d4b-a788-1ac9e32b1192)

![PSS (2)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/574cd1b8-5379-4908-9607-578ac1e39438)

![PSS (3)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/df5b1c34-38f8-4c99-9ec6-40bac3ae4299)

![PSS (4)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/5de5103e-d015-48b9-90f0-6f5ffa05d79d)

![PSS (5)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/be429a9f-2fb1-438a-b927-64f95c9cfbea)

![PSS (6)](https://github.com/jarsheenkaur/Global-Super-Store-Sales-Dashboard/assets/152518497/9b98ce90-ac79-4fd6-bd71-44c39edab543)

## Key Insights

1. Over the three-month period (May to July 2022), AtliQ Grands Hospitality generated **Revenue** of **1.7 billion INR**, with an **Average Customer Rating** of **3.62 out of 5**. During this time, the company received a total of **134,590 Bookings**. The key performance metrics showed an average **Occupancy Rate** of **60%**, a **Cancellation Rate** of **25%**, and a **Revenue Realization Rate** (successful bookings) of approximately **70%**.
2. Trend analysis shows that the **revenue drop** is primarily driven by a **decline in bookings and occupancy rates**. **Cancellation rates**, which have **remained consistent at 24-25%**, do not seem to directly contribute to the revenue decline. However, reducing cancellations could improve capacity utilization and boost overall revenue.
3. **Mumbai** leads the **revenue at 669 million INR**, which aligns with it being a major financial hub and a prime location for business travellers.
4. **AtliQ Exotica (320 million INR)** and **AtliQ Palace (304 million INR)** were top revenue generators, while the **Elite room class** generated **560 million INR**. The **Luxury hotel segment** brought in **1.053 billion INR** overall. This aligns with global trends where high-net-worth travelers continue to show a preference for upscale experiences, but expectations for personalized services are also on the rise.
5. A significant **40% of bookings** came from the **Others** platform, followed by **Makeyoutrip** at **20%**. Unidentified booking sources under "Others" require further investigation for targeted marketing.
6. AtliQ Grands earned **INR 199 million** in revenue from booking **cancellation fees**.
7. Out of a total of 134,590 bookings, 94,411 were successfully completed, 33,420 were cancelled, and 6,759 resulted in no-shows.
8. In the AtliQ Grands project, the highest booking contributors were led by **Mumbai** with 43,000 bookings. Among the properties, **AtliQ Palace** accounted for 17.5% of the total bookings, closely followed by **AtliQ Exotica** at 17.4%. For booking platforms, the **Others** category contributed the largest share with 55,000 bookings, while **Makeyoutrip** added 7,000 bookings. In terms of room preferences, the **Elite room class** saw the highest demand with 49,500 bookings, and the **Luxury hotel category** led with 83,700 bookings. These categories significantly contributed to the overall booking performance at AtliQ Grands.
9. In the AtliQ Grands project, the **Daily Booked Room Nights (DBRN)** was calculated at 1,463, with a total of **Daily Sellable Room Nights (DSRN)** at 2,528 and **Daily Utilized Room Nights (DURN)** at 1,026. This indicates that while 58% of available rooms were utilized (DURN/DSRN), a significant portion of the inventory—around 42%—remained unsold daily. Furthermore, out of the booked rooms (DBRN), only 70% were ultimately utilized, highlighting a 30% gap due to cancellations or no-shows. These metrics suggest that while bookings are consistent, there is potential to improve both occupancy and conversion of bookings into actual stays, optimizing room utilization and overall revenue.
10. The **Average Daily Rate (ADR)** was calculated at **12.7K INR**, indicating AtliQ Grands is operating within the premium segment of the market. India's luxury hotel ADR averages around INR 9K-12K, with high-end properties in Mumbai and Delhi maintaining the upper range. The **Average Length of Stay (ALOS)** was found to be **2 days**, suggesting that guests are staying for a moderate duration. Additionally, the **Average Booking Window (ABW)** of **4 days** highlights a relatively short lead time for reservations, indicating a potential opportunity to encourage earlier bookings through targeted marketing strategies or promotional offers. Collectively, these metrics provide insights into the pricing, guest behavior, and booking patterns at AtliQ Grands, which can be leveraged to optimize revenue and enhance overall performance.
11. **AtliQ Blu** boasts the **highest occupancy rate** at **62%**, closely followed by **AtliQ Palace** at **60%** and **AtliQ City** at **59.5%**. Interestingly, while **Delhi** has the **highest occupancy percentage** among the cities, it contributes the **least** to **overall revenue**, suggesting that higher occupancy does not necessarily translate to higher profitability in that market. Conversely, **Bangalore** exhibits the **lowest occupancy rate** but ranks as the **second highest city in revenue contribution**, indicating that its guests may be opting for higher-priced offerings or extended stays. These dynamics highlight the need for a strategic review of pricing and marketing approaches across different locations to enhance revenue generation while balancing occupancy levels.
12. **AtliQ Seasons** is underperforming significantly, contributing the **least** to **revenue** at **66 million INR**. It has the **lowest average rating** of **2 out of 5** and an **occupancy rate** of only **44.6%**, having received just **3,980 bookings** over the three-month period. This performance is concerning, as it indicates challenges in attracting guests and meeting customer expectations. The combination of low revenue, poor ratings, and occupancy suggests an urgent need for a strategic overhaul, including improvements in service quality, marketing efforts, and possibly revisiting pricing strategies to enhance its appeal and performance in the competitive hospitality market.
