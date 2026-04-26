# NFL-Pass-Rush-Analysis-using-Tracking-Data
Overview

This project analyzes NFL pass rush behavior using player tracking data from
https://www.kaggle.com/competitions/nfl-big-data-bowl-2021 the NFL Big Data Bowl. The goal is to understand how defensive alignment, movement patterns, and situational context influence quarterback pressure.

Key Contributions
Engineered alignment features (head_up, inside_shade, off_tackle, wide9_plus)
Built trajectory-based clustering of pass rushers
Developed an expected pressure model using logistic regression
Introduced a custom STRAIN metric to measure closing speed
Applied Dynamic Time Warping (DTW) for sequence-based clustering
Dataset
NFL Big Data Bowl Tracking Data
Play-level data (EPA, pass result, number of rushers)
Methodology
Filtered traditional dropback pass plays
Created alignment buckets based on distance from the ball
Converted trajectories into fixed-length vectors
Applied clustering (KMeans + DTW)
Built a predictive model for pressure probability
Results
Majority of rushers align off-tackle (~87%)
Edge rushers generate higher pressure rates
Model successfully estimates expected pressure
Identified rush types: speed, power, interior, counter
Example Visualization




Technologies Used
Python (Pandas, NumPy, Scikit-learn)
Matplotlib
DTW (dtaidistance)
Jupyter Notebook
Future Work
Incorporate down & distance
Add double-team data (PFF)
Improve spin move detection
Use advanced models (XGBoost, Neural Networks)
How to Run
pip install -r requirements.txt

Open the notebook:

jupyter notebook notebooks/pass_rush_analysis.ipynb
Author

Jordan Morris
