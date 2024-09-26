# AtliQ Grands Hospitality Analysis Report [Power BI]
Developed an extensive Power BI Dashboard for Revenue Management team of AtliQ Grands utilizing Power Query for data transformation, DAX for custom measures, and a variety of Power BI visualizations for effective data representation. The dashboard offers a comprehensive overview of key performance metrics, revenue sources, booking trends, and property-specific insights. Interactive features like data filters and page navigation facilitate easy exploration of data subsets, enabling AtliQ Grands to optimize pricing, enhance marketing strategies, and improve operational efficiency to regain market share and revenue in the luxury/business hotels segment.

## Problem Statement

**Provide Insights to the Revenue Team in the Hospitality Domain**

**Domain:**  Hospitality       **Function:** Revenue

AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue. However, they do not have an in-house data analytics team to provide them with these insights.
Their revenue management team had decided to hire a 3rd party service provider to provide them with insights from their historical data.

## About Data

The data as well as the problem statement are part of Codebasics Resume Challenge #1 (https://codebasics.io/challenge/codebasics-resume-project-challenge). It consists of the following 5 Tables (as CSV files) :-

Table dim_date contains 4 columns and 92 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| date                | This column represents the dates present in May, June and July.                                                                                     |
| mmm yy              | This column represents the date in the format of mmm yy (monthname year).                                                                           |
| week no             | This column represents the unique week number for that particular date.                                                                             |
| day_type            | This column represents whether the given day is Weekend or Weekeday.                                                                                |

Table dim_hotels contains 4 columns and 25 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                        |
| property_name       | This column represents the name of each hotel.                                                                                                      |
| category            | This column determines which class[Luxury, Business] a particular hotel/property belongs to.                                                        | 
| city                | This column represents where the particular hotel/property resides in.                                                                              |

Table dim_rooms contains 2 columns and 4 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| room_id             | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| room_class          | This column represents to which class[Standard, Elite, Premium, Presidential] particular room type belongs.                                         |

Table fact_aggregated_bookings contains 5 columns and 9,200 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                        |
| check_in_date       | This column represents all the check_in_dates of the customers.                                                                                     |
| room_category       | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| successful_bookings | This column represents all the successful room bookings that happen for a particular room type in that hotel on that particular date.               |
| capacity            | This column represents the maximum count of rooms available for a particular room type in that hotel on that particular date.                       |


Table fact_bookings contains 12 columns and 134,590 rows.
| Column              | Description                                                                                                                                         |
| :-------------------| :---------------------------------------------------------------------------------------------------------------------------------------------------|
| booking_id          | This column represents the Unique Booking ID for each customer when they booked their rooms.                                                        | 
| property_id         | This column represents the Unique ID for each of the hotels.                                                                                        | 
| booking_date        | This column represents the date on which the customer booked their rooms.                                                                           | 
| check_in_date       | This column represents the date on which the customer check-in(entered) at the hotel.                                                               |
| check_out_date      | This column represents the date on which the customer check-out(left) of the hotel.                                                                 |
| no_guests           | This column represents the number of guests who stayed in a particular room in that hotel.                                                          |
| room_category       | This column represents the type of room[RT1, RT2, RT3, RT4] in a hotel.                                                                             |
| booking_platform    | This column represents in which way the customer booked his room.                                                                                   | 
| ratings_given       | This column represents the ratings given by the customer for hotel services.                                                                        | 
| booking_status      |  This column represents whether the customer cancelled his booking [Cancelled], successfully stayed in the hotel [Checked Out] or booked his room but not stayed in the hotel [No show].                                                                                                                                          | 
| revenue_generated   | This column represents the amount of money generated by the hotel from a particular customer.                                                       |
| revenue_realized:   | This column represents the final amount of money that goes to the hotel based on booking status. If the booking status is cancelled, then 40% of the revenue generated is deducted and the remaining is refunded to the customer. If the booking status is Checked Out/No show, then full revenue generated will goes to hotels. |

## Dashboard Features

- 4 Different Dashboards for Quick Insights
- Multiple Data Filters
- Navigation Pane
- Monthly and Weekly Trends for Key Metrices
- Revenue, Booking and Property Analysis done on basis of Various Parameters.
- Drill Down available for Booking % and Revenue Contribution %.

## List of KPIs created using DAX

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

1. Over the 3 Months (May, June and July 2022), AtliQ Grands Hospitality earned  1.7 Billion, achieved Average Rating of 3.62/5, recived 134.59K Bookings as well as Occupancy, Cancellation and Realisation was calculated at about 60%, 25% and 70% respectively.
2. From Trend Charts, it can inferred that drop in Revenue is caused by drop in Bookings and Occupancy %. Cancellation % does not seems to be the reason for drop in Revenue since it has been pretty consistent from 24-25% throughout the months. Still, AtliQ Grands should try to reduce it for achieving better utilization of capacity.
3. Highest Revenue Contributors by Various Categories:- City -> Mumbai (669 Millions approx.), Properties -> AtliQ Exotica (320 Millions) and AtliQ Palace (304 Millions), Room Class -> Elite (560 Millions) and Room (or Hotel) Category -> Luxury (1053 Millions approx). Others at 40% is the highest contributing Booking Platform followed by Makeyoutrip at 20% (Unrecognized booking sources need to be identified for better marketing efforts).
4. AtliQ Grands earned 199 Millions in Revenue as Bookings Cancellation Fees.
5. Out of Total 134590 Bookings, 94411 were Success, 33420 were Cancelled and 6759 were No Show.
6. Highest Bookings Contributors by Various Categories:- City -> Mumbai (43K), Properties -> AtliQ Palace (17.5%) and AtliQ Exotica (17.4%), Booking Platforms -> Others (55K) and Makeyoutrip (7K), Room Class -> Elite (49.5K) and Room (or Hotel) Category -> Luxury (83.7K).
7. Daily Booked Room Nights (DBRN) was calculated at 1463, Daily Sellable Room Nights (DSRN) was calculated at 2528 and Daily Utilized Room Nights (DURN) was calculated at 1026. All of these were consistent over 3 Months with very little variations.
8. Average Daily Rate (ADR) was calculated to be 12.7K, Average Length of Stay (ALOS) was calculated to be 2 days and Average Booking Window (ABW) was calculated to be 4 days. All of these were consistent over 3 Months with very little variations.
9. AtliQ Blu has the Highest Occupancy % of 62% closely followed by AtliQ Palace at 60% and AtliQ City at 59.5%. Delhi has the highest Occupancy % but still is the city with lowest contribution to Revenue. Bangalore has the lowest Occupancy % but still is the second highest city contributing to Revenue.
10. AtliQ Seasons is contributing less towards Revenue, have lowest Average Rating (2/5) as well as lowest Occupancy % (44.6%) as it received only 3.98K Bookings over 3 Months  which is a matter of concern.
