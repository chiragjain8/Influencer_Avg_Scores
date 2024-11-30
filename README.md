# Influencer Average Score Calculation : Documentation
## Project Overview
In the competitive world of social media marketing, selecting the right influencer is crucial for campaign success. This project is focused on building a data-driven system to evaluate influencers' performance across multiple videos, enabling brands to make informed decisions.
## Problem Statement
With a dataset containing ~200 videos and their performance metrics, we aim to:

Identify unique influencers appearing in the videos.<br />
Calculate the average performance of each influencer.<br />
Provide a visualized report showcasing influencers with their associated metrics to help brands identify consistent high performers.
## Objectives
Influencer Identification: Use facial recognition to identify unique influencers across the dataset.<br />
Performance Analysis: Calculate the average performance of each identified influencer.<br />
Actionable Insights: Generate a visual table displaying:<br />
Each influencer’s face.<br />
Their average performance score.<br />
Solution Design
## High-Level Workflow

### Data Preprocessing

Download and extract videos from the provided dataset.<br />
Clean and organize video metadata.<br />
Remove duplicate videos from Data Set.<br />
### Face Detection & Extraction

Used YOLOv8 for accurate face detection and Extraction (Tried 2-3 more models).

### Feature Extraction from Images and Clustering 

Feature Extraction: Used ORB to extract features for each image.<br />
Similarity Matrix: Matched features between images to calculate similarities.<br />
Clustering: Used Agglomerative Clustering to group images based on similarity.<br />

### Performance Aggregation

Associate performance metrics with identified influencers.<br />
Calculate average scores for each influencer.<br />

### Deliverables

A pdf showcasing influencers’ faces alongside their average performance.

## Technical Approach

![flow_ass](https://github.com/user-attachments/assets/60b8c1b7-496e-4c77-b1ff-b8cf4e2074b7)
### Features
1. Video Downloading: Automates downloading videos from URLs listed in an Excel file.
2. Metadata Management: Creates metadata for videos, including their scores and file paths.
3. Duplicate Removal: Identifies and removes duplicate videos using perceptual hashing.
4. Face Detection: Extracts unique faces from videos using YOLOv8 and face_recognition.
5. Clustering: Groups similar faces based on visual similarity for analysis.
6. Score Calculation: Computes average scores for each cluster based on video metadata.
7. Visualization and Reporting: Displays cluster results and saves them to a PDF for documentation.

## Deliverables
GitHub Repository: Fully functional code hosted on GitHub.

Output Table: A PDF report showcasing influencer Picture and performance.

Documentation: Clear instructions in the README.md to guide users through the project.

## Output Preview
![image](https://github.com/user-attachments/assets/e13afd47-c526-4c6b-9f3e-045f69a8af3c)
![image](https://github.com/user-attachments/assets/8631f8c5-38f8-4c8c-b14d-d1cc0291f14c)
![image](https://github.com/user-attachments/assets/fb7c3332-92f3-424e-8b55-df06691d4702)


## Why This Matters
This analysis directly impacts influencer selection strategies by:

Providing quantitative insights into influencer performance.</br>
Helping brands make data-driven decisions about campaign investments.</br>
Enabling the prediction of consistent high performers in social media campaigns.

## Future Enhancements
1. Integrate advanced models like Vision Transformers for face detection.
2. Enhance clustering with deep clustering algorithms (e.g., DBSCAN).
3. Add support for real-time video processing.
4. Integrate additional metrics for cluster evaluation.
5. Enable deployment as a web service for scalability.
