# Analyzing YouTube Trending Videos: What Makes a Video Go Viral?
## Project Proposal — DSA210 Term Project

### Motivation  
YouTube is one of the world’s largest content platforms, where thousands of videos are uploaded every day. However, only a small portion of them become “Trending.”
This project aims to understand **what makes a video go viral globally** by exploring view counts, engagement metrics, upload timing, and video characteristics.

The goal is to answer:

- Which features influence video popularity?

- Do categories matter?

- Does upload time impact views?

- Are likes a good indicator of popularity?

This analysis is based on the publicly available **YouTube Trending Video Dataset** from Kaggle.

The link to the datasets that was used: https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset

---

### Contents
- [Motivation](#motivation)
- [Data Source](#data-source)
- [Methodology](#methodology)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Hypothesis Tests](#hypothesis-tests)
- [Expected Outcomes](#expected-outcomes)
- [Ethical Considerations](#ethical-considerations)

  
---

## Dataset  
### Source 
 Kaggle — "YouTube Trending Video Dataset"
Dataset includes trending videos across multiple countries with columns such as:

- video_id, title, publishedAt, channelTitle
- categoryId, tags, view_count
- likes, dislikes, comment_count
- description, trending_date, comments_disabled

This dataset is the global trending sample used for this project.
All data used will be **publicly available** and contain no personal information.

---

### Methodology  
1. **Data Collection:** Download the dataset and gather category info from YouTube API.  
2. **Data Cleaning:** Handle missing values, duplicates, and fix column types.  
3. **Exploratory Data Analysis (EDA):**  
   - Top trending categories  
   - Relation between likes, views, and comments  
   - Timing patterns (day of week, publish hour)  
4. **Machine Learning:**  
   - Predict view count or like ratio using regression models  
5. **Visualization & Reporting:**  
   - Use Python libraries (matplotlib, seaborn, pandas) for charts and insights  

---
### Feature Engineering 
Because DSA210 requires data enrichment, I created additional meaningful features:

**Time-based features**
- publish_hour
- publish_day
- publish_month
  
**Text-based features**
- title_length
- description_length
- tag_count
  
**Engagement features**
- like_ratio = likes / view_count
- comment_ratio = comment_count / view_count
- engagement_score = (likes + comment_count) / view_count
  
**Trending behavior**
- days_until_trending = trending_date - publishedAt
  
---
### Exploratory Data Analysis 

**Distributions**
- view_count distribution
- likes distribution
- comments distribution

**Category exploration** 
- category frequency
- category vs view_count (boxplot)

**Engagement & correlation**
- correlation heatmap (views, likes, comments, engagement_score)
- scatterplots (likes vs views, comments vs views)

**Timing patterns**
- publish_hour histogram
- publish_day bar chart

Each graph includes interpretation.

---
### Hypothesis Tests

***HT1 — Category → View Count (ANOVA)***

**H0:** Mean view counts are equal across categories

**H1:** At least one category differs

ANOVA + boxplot + p-value interpretation

***HT2 — Upload Hour → View Count (ANOVA)***

**H0:** Upload hour does not affect view count

**H1:** At least one hour group differs

Hours grouped into morning/afternoon/evening/night

***HT3 — Likes vs Views (Correlation)***

- Pearson correlation test
- Scatter plot + regression line
- p-value interpretation

---
### Expected Outcomes  
- Identify features that most influence video popularity  
- Compare engagement trends across categories  
- Build a small model that predicts video performance  
- Present insights through clean visuals and simple explanations  

---

### Ethical Considerations  
- Only publicly available, non-personal data will be used  
- All sources will be cited properly  
- Any AI assistance (like writing help) will be documented  

---
### Project Conclusions 

In this project, I analyzed trending YouTube videos to understand the factors driving their popularity. Based on my analysis, here are the general takeaways:

***1. Category is Key to Success*** My analysis revealed that the **video category plays a decisive role** in determining view counts. Certain categories, such as Music and Entertainment, consistently show a much higher potential for views compared to others like News or Education. This suggests that the type of content is a more significant factor for virality than random chance.

***2. The "Best Upload Time" Myth*** Contrary to popular belief, I observed that the specific **time of day a video is uploaded does not have a critical impact** on its view count. While there may be slight fluctuations during certain hours, the difference is not significant enough to determine whether a video goes viral or not. Quality content tends to find its audience regardless of the upload hour.

***3. Engagement (Likes) is the Strongest Signal*** I found a **very strong positive relationship** between the number of likes and the total view count. This confirms that user engagement is the most reliable indicator of a video's success and its promotion by the algorithm. High engagement rates are directly linked to broader reach.

***Final Verdict:*** To maximize the chances of a video going viral, **content category** and **viewer engagement (likes)** are the most critical factors. Technical details, such as the exact hour of upload, have a negligible effect on overall success compared to these primary drivers.

---

