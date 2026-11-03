# Social Media & Student Life: Power BI Dashboard

An interactive Power BI dashboard that explores how social media use connects to students' sleep, mental health and academic performance, built from a student survey dataset.

**Author:** Hasna NM
**Dataset:** `Social_media_impact_on_life`
**Tools:** Power BI, DAX

## Project Overview

Social media is part of daily student life and may change how students sleep, feel and study. This project uses student survey data to look at these links in a clear, visual way. The goal is to turn the data into simple charts and useful ideas that can help students.

## Objectives

1. **Understand usage:** see which platforms students use most and how many hours they spend each day.
2. **Check health links:** see how daily usage connects to sleep and mental health scores.
3. **Check study links:** see if students who say their studies are affected use social media more.
4. **Find helpful actions:** turn the findings into simple actions that can support students.

## Dataset

- **File:** `Social_media_impact_on_life`
- **Size:** 1,000 student records
- **Covers:** gender, age, academic level, country, most-used platform, average daily usage hours, sleep hours, mental health score, academic impact (Yes/No) and overall impact (Positive/Neutral/Negative)

## Data Cleaning

**What was done**
- Grouped daily usage hours into simple ranges
- Grouped mental health scores into simple ranges
- Created an **Age Group** column
- Created a **Usage Group** column

**Data quality checks**
- Checked for missing values: none were present
- Checked for duplicate records: none were found
- Corrected data types (Student ID, Age and other columns)
- Reviewed column names and data values for consistency

## Methodology

1. **Load data:** bring the table into Power BI.
2. **Create groups:** Age Group, Usage Group and bins.
3. **Build the report:** 4 pages, with 6 filters on each.

**Filters on every page:** Gender, Academic Level, Country, Platform, Overall Impact, Age Group

## DAX Measures

| Measure | Purpose | Main functions |
|---|---|---|
| Total Student | Number of students | `COUNTROWS()` |
| Average Daily Hours | Average hours used each day | `AVERAGE()` |
| Average Sleep Hour | Average hours slept | `AVERAGE()` |
| Average Mental Health Score | Average mental health score | `AVERAGE()` |
| Academic Impact % | Share of students affected in studies | `DIVIDE()` |
| Most Used Platform | Platform with the most students | `TOPN()`, `COUNTROWS()` |
| Academic Effect % | Overall academic effect of social media | `DIVIDE()`, `CALCULATE()`, `COUNTROWS()` |
| Average Sleep Hours - Affected Students | Average sleep of affected students | `CALCULATE()`, `AVERAGE()` |
| Average Sleep Hours - Non-Affected Students | Average sleep of non-affected students | `CALCULATE()`, `AVERAGE()` |
| Average Usage Affected Students | Average usage of academically affected students | `CALCULATE()` |
| Students Affected Academically | Number of academically affected students | `CALCULATE()`, `COUNTROWS()` |

## Dashboard Pages

The dashboard has 4 pages, each with 6 filters.

### 1. Overview
A quick look at the whole dashboard.

<img width="920" height="513" alt="overview" src="https://github.com/user-attachments/assets/c1c43d5d-c0bc-47ab-8e8d-e73cd2447ae3" />

- **Charts:** Overall impact (donut chart) and academic performance (bar chart)
- **Finding:** 47% of students say social media has a negative impact, and 558 students say their studies are affected.

### 2. Social Media Usage
Which platforms students use and for how long.

<img width="936" height="528" alt="Social" src="https://github.com/user-attachments/assets/e8d1f156-1ecf-4408-82e8-3a7e9e81b6fb" />

- **Charts:** Most-used social media platforms and average daily usage by platform
- **Finding:** LinkedIn and YouTube are the most used platforms (155 students each). Snapchat users spend the most time, 5.4 hours a day.

### 3. Health and Well-being
How usage connects to sleep and mental health.

<img width="957" height="538" alt="health" src="https://github.com/user-attachments/assets/cab858b6-cb06-4d5c-82a4-8363a4ac6e26" />


- **Charts:** Sleep hours by platform and mental health score by platform
- **Finding:** LinkedIn users sleep the most (6.7 hours) and score highest (6.4). Snapchat users sleep the least (6.2 hours) and score lowest (6.1).

### 4. Academic Performance
Whether studies feel the effect of social media.

<img width="938" height="525" alt="academic" src="https://github.com/user-attachments/assets/4ec88685-1471-4145-b485-3c2494a160d1" />


- **Charts:** Daily usage by academic impact and academic impact by educational level
- **Finding:** Students who say their studies are affected use social media 6.0 hours a day, compared with 4.2 hours for the others.

## Key Insights

- **Overall impact:** 47% of students say the impact of social media is negative, 28% say it is positive and 25% say neutral.
- **Studies:** About 56% of students (558 out of 1,000) say their studies are affected.
- **Usage:** Students spend about 5 hours a day on every platform, with little difference between platforms.
- **Health:** The differences in sleep and mental health score between platforms are small (0.5 hours of sleep, 0.3 points).
- **Academic link:** Students who say their studies are affected use social media about 1.8 hours more per day (6.0 vs 4.2 hours).

## Recommendations

- **Support healthy sleep:** share simple sleep tips, such as no phone before bed.
- **Help students focus on studies:** offer study-skills and time-management support.
- **Look after well-being:** make counselling and well-being help easy to find.
- **Keep tracking:** use this dashboard each term to check progress.

## Limitations

- **Links, not causes:** the data shows associations and cannot prove that social media causes a change.
- **Answers may not be exact:** some answers, like sleep or mental health, may be self-reported.
- **One main platform:** each student has one most-used platform, so mixed use is not shown.
- **One moment in time:** the data cannot show how things change over time.
