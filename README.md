# Detecting_Anomalous_Transactions
Dived into the world of banking transactions to uncover hidden anomalies and protected customer confidence

## Anomalous Transaction Detection: Unsupervised Fraud Screening with Isolation Forest (PyOD) | Python, scikit-learn

Used an Isolation Forest to flag unusual banking transactions without labelled fraud data. Each transaction gets an anomaly score from its amount, duration and account balance, the top 5% are flagged, and a histogram compares flagged and normal amounts.

# CONTEXT
A financial compliance scenario: surface transactions that look unlike the rest so analysts can review them first. With no confirmed fraud labels, unsupervised anomaly detection is the natural starting point.

# MY ROLE
I built the scoring, flagging, summary and visualisation.

# WHAT I DID
• Selected three numeric features (TransactionAmount, TransactionDuration, AccountBalance) and trained PyOD's IForest with 100 trees, contamination 0.05 and a fixed random seed
• Added a continuous anomaly score and a binary Anomaly flag for every transaction
• Built a summary table of flagged transactions (ID, amount, duration, balance) for analyst review
• Plotted overlaid histograms of transaction amounts for normal vs anomalous groups, with labelled axes and a legend, and saved the figure as a PNG

# RESULTS
• 126 of 2512 transactions flagged (5%)
• Flagged transactions differed from normal ones mainly in transactions of more than $1200

# TECH STACK
Python, PyOD (IForest), pandas, Matplotlib, seaborn
