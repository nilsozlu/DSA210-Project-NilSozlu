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

---

### Contents
- [Motivation](#motivation)
- [Data Source](#data-source)
- [Methodology](#methodology)
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
### Feature Engineering (Data Enrichment)
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
