# students-performance-analysis-
📊 Students Performance Analysis – Power BI Project This project presents an interactive and visually engaging Power BI dashboard that analyzes student academic performance using various demographic and educational factors. The goal is to uncover insights into how factors such as gender, parental education, lunch type, and test preparation courses influence student scores in math, reading, and writing. 📌 Project Objectives

To explore how different socio-economic and preparatory factors impact student performance.
To build an interactive dashboard that provides quick insights into performance trends.
To demonstrate proficiency in using Power BI features including DAX, data modeling, and visual storytelling. 🧠 Key Insights
Students who completed test preparation courses performed significantly better.
Higher parental education correlates with better average scores.
Female students tended to score higher on reading and writing, while male students did better in math.
Students with standard lunch performed better than those on free/reduced lunch.
📊 Dashboard Features

🎯 KPI Cards - Total students, average math score, and count of students who completed prep 📌 Filters / Slicers - Gender, parental education, lunch type, and test prep course
📈 Bar Chart - Average score by gender
🥧 Pie Chart - Performance category distribution (Excellent, Good, Average, Needs Improvement) 📊 Column Chart - Impact of test prep on scores
📉 Table Visual - Score summaries (Total & Average)
🧰 Tools & Technologies

Power BI Desktop

Power Query Editor for data cleaning

DAX (Data Analysis Expressions) for calculated columns and measures

CSV as data source

FORMULAS USED high math count = COUNTX(FILTER('StudentsPerformance','StudentsPerformance'[math score]>50),'StudentsPerformance'[math score])

high reading count = COUNTX(FILTER('StudentsPerformance','StudentsPerformance'[reading score]>50),'StudentsPerformance'[reading score])

high writing score = COUNTX(FILTER('StudentsPerformance','StudentsPerformance'[writing score]>50),'StudentsPerformance'[writing score])

parentid = COUNTAX('StudentsPerformance','StudentsPerformance'[parental level of education])

total overall score = SUMX('StudentsPerformance','StudentsPerformance'[math score]+'StudentsPerformance'[reading score]+'StudentsPerformance'[writing score])

unique parental level = DISTINCTCOUNT('StudentsPerformance'[parental level of education])

Average score = AVERAGE('StudentsPerformance'[total score])

average math score = AVERAGE('StudentsPerformance'[math score])

Complete prep students = CALCULATE(COUNTROWS('StudentsPerformance'),('StudentsPerformance'[test preparation course]="completed"))

performance category = VAR avg_score=('StudentsPerformance'[math score]+'StudentsPerformance'[reading score]+'StudentsPerformance'[writing score])/3 RETURN IF(avg_score>90,"Excellent",IF(avg_score>75,"Good",IF(avg_score>50,"Average","Need Improvement")))

Student count = COUNTROWS('StudentsPerformance')

total score = ('StudentsPerformance'[math score]+'StudentsPerformance'[reading score]+'StudentsPerformance'[writing score])

Unique Parent Education levels = CALCULATE(DISTINCTCOUNT('StudentsPerformance'[parental level of education]))

