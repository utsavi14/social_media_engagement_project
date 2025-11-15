# 📊 Social Media Engagement Analysis  
### Final Capstone Project – Customer Analytics  
### By: **Utsavi Sunil Patel**

This project analyzes what drives Instagram engagement using the **CRISP-DM** framework.  
The goal is to help brands understand **what to post, when to post, and how to write captions/hashtags** in order to increase their engagement rate.

---

## 1. Business Understanding

Instagram engagement is inconsistent — some posts perform very well, while others get very low interaction.  
The brand does not have data-driven answers for:

- What type of posts perform better  
- How many hashtags should be used  
- What caption length works  
- When is the best time to post  

### **Project Goal**  
To develop simple, data-driven rules that can improve Instagram engagement by **20%–40%**, and provide a clear posting strategy.

---

## 2. Dataset Understanding

Dataset: **instagram_reach.csv**  
Rows: 100  
Each row represents one Instagram post.

### **Features include:**
- Caption  
- Hashtags  
- Likes  
- Followers  
- Time Since Posted  
- (Engineered features created later)

### **Why this dataset is suitable**
- Contains customer engagement signals  
- Includes content, timing, and audience size  
- Matches the project’s business goals  
- Simple and realistic social media data  

### **Limitations**
- Missing captions/hashtags in some rows  
- Time stored in text (“3 days”, “2 hours”)  
- No post type or image data  

---

## 3. Data Preparation

### **Main cleaning steps:**
- Removed unnecessary index columns  
- Filled missing captions/hashtags with empty strings  
- Converted “Time since posted” into numeric **hours**  
- Cleaned text (lowercase, stripped spaces)

### **Engineered Features**
- `caption_length`  
- `hashtag_count`  
- `engagement_rate` (likes ÷ followers)  
- `hours_since_posted`  

These features help understand what actually drives engagement.

---

## 4. Exploratory Data Analysis (EDA)

### 🔹 **Insight 1 — Hashtags**
- Engagement stays low across all hashtag counts  
- No strong pattern  
➡ **Hashtags do NOT strongly affect engagement**

### 🔹 **Insight 2 — Caption Length**
- Very long captions underperform  
- Short/medium captions slightly better  
➡ **Caption length has weak impact**

### 🔹 **Insight 3 — Timing (Freshness)**
- Posts within **0–5 hours** get the highest likes  
- Engagement drops sharply after **10 hours**  
➡ **Timing is the strongest factor**

---

## 5. Modeling

### **Target Variable**
High vs Low engagement (based on median engagement rate)

### **Models Used**
1. **Logistic Regression** (baseline)
2. **Decision Tree Classifier** (improved model)

### **Results**
- Logistic Regression Accuracy: **85%**
- Decision Tree Accuracy: **70%**

### **Feature Importance (Decision Tree)**
1. Followers — strongest  
2. Hours Since Posted  
3. Hashtag Count  
4. Caption Length — weakest  

### **Business Impact**
Using these insights, brands can increase engagement by **20–40%** simply by optimizing posting times and growing their follower base.

---

## 6. Recommendations

Based on EDA and modeling:

### ✔ Post during high-engagement hours  
Fresh posts perform best.

### ✔ Focus on growing followers  
Largest driver of engagement.

### ✔ Use 3–6 relevant hashtags  
More hashtags do not guarantee higher engagement.

### ✔ Keep captions simple  
Length has minimal effect.

### ✔ Track posting patterns  
Monitor which hours and days perform best.

---

## 7. Next Steps (Future Work)

If more data is available, the analysis can be expanded by adding:

- Post type (photo, reel, video)  
- Caption sentiment  
- Image content (computer vision)  
- Exact posting timestamps  
- Audience demographics  

---

## Project Files

| File | Description |
|------|-------------|
| `capstone.ipynb` | Full analysis + code |
| `capstone.html` | HTML export of the notebook |
| `Capstone_Instagram_Final_PPT_With_ThankYou.pptx` | Executive presentation |
| `instagram_reach.csv` | Dataset |
| `README.md` | This file |

---

## Author

**Utsavi Sunil Patel**  
Master’s in Data Science – Customer Analytics  

GitHub: https://github.com/utsavi14  
