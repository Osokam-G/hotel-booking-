# Hotel Booking Performance Analysis

> An analysis of hotel booking performance, reservation outcomes, hotel type, guest origin, and booking volume by arrival month.

## 1. Introduction

This project analyzes hotel booking records to understand booking volume and the outcomes of reservations across City Hotels and Resort Hotels. The accompanying dashboard summarizes total bookings, completed stays, cancellations, no-shows, country of origin, and monthly arrival patterns.

This analysis covers **119,208 total bookings**: **75,010 completed stays (Check-Out)** and **44,198 non-completions** (cancellations and no-shows). 

## 2. Problem Statement

Hotels need a clear view of how many reservations convert into completed stays, how cancellation and no-show volumes vary by hotel type, and where guests originate. Without a consolidated view, it is harder to identify booking patterns and areas that may warrant operational attention.

This analysis addresses the following questions:

- How many bookings were recorded, and what share resulted in a completed stay?
- How do booking and non-completion volumes compare between City Hotels and Resort Hotels?
- Which guest-origin countries contribute the most bookings?
- How does booking volume vary by arrival month?

## 3. Data Sourcing
The data is originally from the article Hotel Booking Demand Datasets, written by Nuno Antonio, Ana 
Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019.
- Dataset name and publisher: `Hotel Booking dataset`
- Dataset version or retrieval date: `February 2019.`
- Relevant fields: hotel type, reservation status, country, and arrival date/month 

## 4. Data Transformation and Cleaning

1. **Excel — initial inspection:** I reviewed the dataset structure, columns, sample values, and apparent data quality issues.
2. **Google Colab — cleaning:** I cleaned and transformed the data for analysis. where I treat  missing values, data types, duplicates.

    **view of the cleaned dataset on MS EXCEL**

<img width="1920" height="1010" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/5b9c6f81-384e-4eec-9952-b779005dea8e" />

3. **Power Query — validation:** I performed additional checks on the prepared dataset to confirm that fields and values were suitable for reporting before loading it into Power-BI for visualization.

**view of the dataset on power query**

<img width="1920" height="1080" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/b6749fb9-8148-485c-952d-662d8818fd38" />


## 5. Analytical Measures

| Measure | Dashboard value | Meaning |
|---|---:|---|
| Total Bookings | 119,208 | All bookings represented in the dataset |
| Completed Stays | 75,010 | Bookings with `Check-Out` status |
| Canceled and No-Show Bookings | 44,198 | Canceled bookings plus no-shows |
| Non-Completion Rate | 37.08% |the rate of Canceled and no-show bookings  |
| Completed Stay Rate | 62.92% | the rate of Completed stays bookings |

breakdown of outcome by hotel type:

| Hotel | Canceled | Check-Out | No-Show | Total |
|---|---:|---:|---:|---:|
| Resort Hotel | 10,829 | 28,926 | 291 | 40,046 |
| City Hotel | 32,163 | 46,084 | 915 | 79,162 |
| **Total** | **42,992** | **75,010** | **1,206** | **119,208** |


## 6. Dashboard and Visuals:

- KPI cards for total bookings, canceled and no-show bookings, non-completion rate, completed stay rate, and completed stays.
  
- A horizontal bar chart of bookings by guest country.
Portugal has the highest booking count by a wide margin, followed by the United Kingdom and France. The chart shows where bookings originated.


<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/b42e84c5-0330-4d4b-b62e-7f51485fae07" />


  
- A comparison of total bookings by hotel type.
  
City Hotels have more bookings than Resort Hotels—about 79,162 compared with 40,046.


<img width="1920" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/8dbb0a81-f23d-4524-8790-58411f2c8ff4" />

  
- A donut chart of reservation outcomes (`Check-Out`, `Canceled`, and `No-Show`).

  
75,010 bookings ended in a completed stay (Check-Out), while 42,992 were canceled and 1,206 were no-shows. The completed stay rate is 62.92%



<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/ef74ea2a-d602-47e6-84b1-0e9767bd1f58" />



- A hotel-by-status summary table.

  
City Hotels have higher counts across the displayed outcomes, including cancellations. These are booking counts; rates would give a fairer comparison between hotel types.



<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/e2ed772e-a519-4d7c-ab59-660874706ca7" />



- A bar chart comparing canceled and no-show bookings by hotel.

  
City Hotels show substantially more cancellations and no-shows than Resort Hotels. This may merit further investigation.



<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/66b76264-22df-477c-9b5b-75c912157e1d" />



- A monthly area chart of bookings by arrival month.

  
August has the highest booking volume in the chart, while January has the lowest. The months appear sorted by volume, so this chart doesn’t show the chronological pattern across the year.


  
<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/7e9b7c52-21ed-44db-8459-ca3072d7be00" />



- Country and customer-related slicers for interactive filtering.

  

## 7. General Insights

- The dataset contains **119,208 bookings**, of which **75,010 (62.92%)** are completed stays.
- **44,198 bookings (37.08%)** are cancellations or no-shows combined. The table separates these into **42,992 cancellations** and **1,206 no-shows**.
- City Hotels account for **79,162 bookings**, compared with **40,046** for Resort Hotels. They also have higher counts of cancellations (32,163 versus 10,829) and no-shows (915 versus 291). 
- Portugal (PRT) is the largest country category shown, followed by the United Kingdom (GBR) and France (FRA). 
- The displayed monthly chart is ordered by booking volume rather than calendar sequence. August appears highest and January lowest among the shown categories.
## 8. Recommendation

- Investigate the high cancellation count at City Hotels by comparing cancellation **rates** by hotel type, season, lead time, market segment, and other relevant factors. Counts alone do not establish the cause.
- Review cancellation and no-show patterns separately. No-shows are a smaller count in this dataset, so operational responses should be proportionate and evidence-based.
- Use arrival-month patterns to plan staffing and capacity after confirming the month sort order and whether all months represent comparable periods.
- Validate country completeness and standardization before using country rankings for marketing or market allocation.
- Track completed-stay and non-completion rates over time so future decisions can be evaluated against a consistent baseline.

## 9. Conclusion

This project provides a consolidated view of hotel booking volume and reservation outcomes. The dashboard shows that completed stays make up 62.92% of the 119,208 bookings, while 37.08% ended in cancellation or no-show. Hotel type, guest country, and arrival month provide useful starting points for deeper analysis. Follow-up work should focus on normalized rates, validated date ordering, and documented data-quality rules before drawing causal conclusions.

## 10. Author

**OSOKAM GIFT**  
[LinkedIn](add-your-link) · [Portfolio](add-your-link) · [GitHub](add-your-link)

