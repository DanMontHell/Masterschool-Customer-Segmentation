# 🧭 Customer Segmentation for Loyalty Program

This project identifies key customer segments using app session data, booking behavior, and demographic info, to support the design of a targeted loyalty program. The database was queried using SQL and Python was used for EDA, preprocessing and unsupervised machine learning.

## 📌 Objective

To segment loyal customers and match each segment to a relevant perk for our loyalty program helping improve retention, reward personalization, and marketing strategy.

---

## 📊 Dataset

Data was sourced from four tables:
- **Users**: Demographics and sign-up date
- **Sessions**: App activity and bookings
- **Flights**: Booking and baggage behavior
- **Hotels**: Stay details and spend

Loyal users were defined as those with **7+ sessions since Jan 2023**.

🔗 **Database Connection:**
`postgresql://Test:bQNxVzJL4g6u@ep-noisy-flower-846766.us-east-2.aws.neon.tech/TravelTide`

---

## 🔍 Methodology

### 1. Data Preprocessing
- Combined tables via SQL
- Fixed data issues (e.g. recalculated nights stayed using check-in/out timestamps)
- Scaled features and used PCA to explore dimensionality

### 2. Clustering & Evaluation
Tested multiple algorithms:
- **K-Means** (chosen model)
- **OPTICS** (best silhouette score but poor clustering)
- **DBSCAN** (poor clustoring and scoring)
- **Hierarchical** (decent clustering)

Final model selected based on interpretability and alignment with real user behavior.

### 3. Segment Profiling
Mapped cluster behavior to interpretable groups:
- 🧳 Long Stay Traveller
- 💼 Business Traveller
- 🔁 Frequent Discount Booker
- 👨‍👩‍👧 Family Booker
- 🙋‍♂️ Solo Traveller

### 4. Perk Recommendations
| Segment                  | Recommended Perk              |
|--------------------------|-------------------------------|
| Long Stay Traveller      | One free hotel night          |
| Business Traveller       | Free hotel meal               |
| Frequent Discount Booker | Exclusive discounts           |
| Family Booker            | Free checked bag              |
| Solo Traveller           | No cancellation fee           |

---

## 🛠 Skills Used

- **Python**: pandas, NumPy, scikit-learn, matplotlib, seaborn
- **SQL**: Joins, filtering, calculated fields, CTEs
- **Data Cleaning**: Handling nulls, fixing incorrect values, recalculating features
- **Clustering**: OPTICS, K-Means, Hierarchical, PCA for dimensionality reduction
- **Data Visualization**: Histograms, box plots, scatter plots etc.
- **Stakeholder Communication**: One-page report, presentation, perk strategy

## 💾 Files

- `segmented_customers.csv`: Final dataset with segment labels
- `Daniel_Hellmuth_DA109_Mastery_Project_TravelTide_Customer_Segmentation.ipynb`: Script for model training and clustering
- `Daniel Hellmuth DA109 TravelTide Executive Summary.pdf`: Summary report for stakeholder meeting
- `Daniel Hellmuth DA109_ TravelTide Customer Segments .pdf`: Customer segmentation presentation for marketing meeting

## ✅ Next Steps

- Approve segment definitions and perk alignment
- Add “loyalty” and “segment” tags to user database
- Launch test email campaign with segment-specific messaging
- Track loyalty sign-ups and monitor performance

---

## 📫 **Explore Further**  
**[LinkedIn](https://www.linkedin.com/in/danhellmuth/)**  
**[GitHub](https://github.com/DanMontHell)**  
**[Tableau](https://public.tableau.com/app/profile/daniel.montreal.hellmuth/vizzes)**  
