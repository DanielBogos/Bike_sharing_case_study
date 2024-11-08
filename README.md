# Bike_sharing_case_study
### Project Overview
Heeeeey! First project of mine so far...
This project analyses a dataset from a virtual bike sharing company named **Cyclistic bike-share**.
The objective was to determine if there is an opportunity for future company growth by implementing marketing efforts that focus on converting casual riders to members. 
However, using multiple metrics and charts throughout my analysis, the findings indicate that the number of casual riders is relatively low, suggesting limited potential for conversion and more important, the casual riders seem to differ quite a bit from the members when comparing the behavior.
  
## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Key Findings](#key-findings)
5. [Files in This Repository](#files-in-this-repository)
6. [Technologies Used](#technologies-used)
7. [Conclusion](#conclusion)
   
## Dataset
- **Source**: The dataset was provided by the bike-sharing company and includes information ride_id, beginning and the end of the journey, user type (casual or member), time and date, station_id and other ride characteristics.
- **Key Fields**:
  - **ride_id**: Every ride has an unique id.
  - **rideable_type**: Indicates the type of the bike (classic or electric).
  - **started_at**: Indicates the time and date at the start of the trip.
  - **ended_at**: Indicates the time and date at the end of the trip.
  - **member_casual**: Indicates whether a rider is a casual rider or a member.

## Methodology
1. **Data Cleaning**: Performed initial data cleaning to remove duplicates and correct inconsistencies such:
   - missing values in the ride_id column,
   - removing the rows where the time is inconsistent (end trip time earlier than start trip),
   - remove the unnecessary columns,
   - making sure the columns such *member_casul* or *rideable_type* don't any any additional values except the ones that are valid.
2. **Preparing data**:
   * I checked if all columns have the right type of data and did converting when needed.
   * I created columns that will be useful for my analysis such:
   - split the datetime columns (such *started_at*) into 2 sepparate columns (*date* and *time*),
   - create a column *ride_length* that shows the duration of each trip,
   - create 2 columns: *day_of_week* and *month*.    
3. **Exploratory Data Analysis (EDA)**: Analyzed trip patterns by month, season, day of the week, time of the day and ride duration.
4. **Comparative Analysis**: Compared behaviors between casual riders and members across various metrics such:
   - average trip duration,
   - peak usage times during the day,
   - number of rides by day of the week, month and season,
   - distribution of electric vs classic bikes.
6. **Statistical Testing**: Applied statistical tests to identify significant differences between casual riders and members such:
   **Is the 2:1 ratio of total rides between casual and membership true for every time frame (month, day of the week or time of the day)**.

## Key Findings
- **Casual Rider Demographics**: Casual riders make up a small proportion of overall users, limiting the potential impact of targeted marketing.
- **Usage Patterns**:
  - Casual riders tend to have longer trip durations especially while using a classic bike type (assuming mainly for leisure)
  - Casual riders don't mind riding in the night or outside "rush hours".
  - Casual rider usage peaks on weekends, while member usage is more consistent throughout the week.
  - I've noticed a significant difference between the two when looking at the number of rides throughout the day where with members, we clearly see peaks in the rush hours (many commute to work) and not so much with casual (the line is rather flat and just steadily goes up throughout the day until it matches the afternoon rush hour).
  - Casual riders love to cycle in the summer and very little in the winter.
- **Limited Conversion Opportunity**: The data suggests limited opportunity to convert casual riders to members due to their low numbers and distinct usage patterns.

## Files in This Repository
- `README.md`: This file, provides an overview of the project.
- `R_markdown_bike_case_study.Rmd`: R Markdown file with the full analysis code and findings.
- `snall_bike_df.csv`: Sample of the dataset used for analysis (due to the size limit, this is only a sample). Full dataset is coming soon.
- `output.html` or `output.pdf`: Rendered report of the R Markdown file for easier viewing of results and visualizations.

## Technologies Used
- **Excel**: Preliminary exploration, data inspection, data cleaning, creating new columns and data visualization.
- **SQL**: Merging the data by season, creating various summaries (averages, counts, grouping, etc)
- **R**: Used for merging all seasons into one big file, data converting, analysis, and visualization.
- **R Markdown**: Documented the analysis, the steps taken and rendered it into HTML and PDF for sharing.

## Conclusion
This analysis suggests that the bike-sharing company’s marketing efforts may not be as effective if focused solely on converting casual riders to members due to their limited numbers and different behavior and preferences. 
Future efforts could explore other approaches, such as:
- promoting membership benefits to existing users with low trip frequency,
- for those who ride in the weekend, a package with multiple rides could be a way to attract them,
- creating different membership plans such 3 or 6 months to attract those who ride in the warmer months,
- focusing on recruiting new members from outside the current user base and bringing more awareness,
- finally, increase the number of electric bike since they help the riders get to their destination much faster, particularly in the winter.

