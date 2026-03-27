📺 YouTube Edu-Analytics: A Full-Stack Machine Learning Pipeline
🚀 Project Overview

This project implements a complete end-to-end Data Science pipeline designed to discover, extract, and categorize educational YouTube channels. Using a data-driven approach, we analyze high-volume metadata to predict a channel's growth category through various Machine Learning classifiers.
📊 Big Data Scale & Robustness

The models are trained on a high-density dataset, ensuring statistically significant results and robust generalization:

    Total Video Metadata: ~490,000 records.

    Unique Channels Analyzed: 10,600 educational creators.

    Domains Analyzed: 90 distinct academic and technical niches.

    Statistical Depth: The massive volume of data allowed for precise Inflection Point Analysis, making the "separation zones" between growth categories mathematically distinct and clear.

🛠️ Pipeline Architecture

The project is structured into four specialized notebooks:

    01_Automated_Channel_Discovery.ipynb: Automated discovery of channel IDs across 90 educational domains using the YouTube API.

    02_High_Throughput_Video_Extraction.ipynb: Mass extraction of video metadata using Python ThreadPoolExecutor for high-speed parallel processing.

    03_Data_Wrangling_and_Feature_Engineering.ipynb:

        Processing and cleaning of 490k records.

        Feature Engineering: Calculating publishing regularity (Coefficient of Variation), engagement metrics, and channel age.

        Statistical Binning: Defining 6 growth classes based on logarithmic inflection points (e.g., 100, 2k, 17k, 160k, 1.2M subs).

    04_Predictive_Modeling_and_Classification.ipynb: Comparative evaluation of multiple classifiers including SVC, Random Forest, KNN, and Logistic Regression.

🏆 Model Performance

The models were tasked with classifying channels into 6 growth stages. The Random Forest Classifier provided the highest overall accuracy.
Model	CV Score (Mean)	Test Accuracy
Random Forest	0.7636	78.72%
SVC (RBF Kernel)	0.7656	0.7806
Logistic Regression	0.7594	0.7735
K-Nearest Neighbors	0.7185	0.7393
Confusion Matrix (Random Forest)

The model shows high precision in identifying core growth categories, with a particularly strong performance in identifying established channels.
💡 Key Findings

    Feature Importance: Metrics like "Publishing Regularity" and "Engagement-per-video" are superior predictors of a channel's category compared to simple total upload counts.

    Model Stability: The minimal gap between Cross-Validation scores (76.56%) and Test Accuracy (78.72%) confirms the quality of the engineered features and the absence of overfitting.

⚖️ License

This project is licensed under the MIT License - see the LICENSE file for details.
