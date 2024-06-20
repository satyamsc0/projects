# AI-Powered Milk Adulteration Detection

**App Link** - https://milk-adulteration-detection.azurewebsites.net/

### Project Overview:

1. Developed a robust image processing pipeline for detecting milk adulterants, including feature extraction using color space conversions and channel splitting (RGB, HSV, LAB). Implemented machine learning models (Decision Tree, Random Forest, XGBoost) to classify images, achieving high accuracy and balanced precision-recall metrics through cross-validation and hyperparameter tuning.

2. Successfully deployed the milk adulteration detection system using Flask API and Docker containerization. Implemented continuous integration and continuous deployment (CI/CD) workflows with GitHub Actions, ensuring scalable and reliable integration into existing dairy industry workflows.


------

### Description of AI-Powered Milk Adulteration Detection Project

**Introduction:**
The AI-Powered Milk Adulteration Detection project addresses the significant challenge of milk adulteration, which poses health risks and economic losses. This project was developed as part of the Post Graduate Program in Artificial Intelligence and Data Science at Jio Institute, aiming to create a robust and efficient solution for detecting adulterants in milk using advanced machine learning and image processing techniques.

**Problem Statement:**
Milk adulteration is a widespread issue, and traditional detection methods are often costly, time-consuming, and labor-intensive. The primary goal of this project is to develop a low-cost, rapid solution for detecting adulterants in milk samples using image analysis of test strips. Initially, the focus was on classifying milk samples as adulterated or non-adulterated, with future goals to quantify the extent of adulteration.

**Project Objectives:**
- Develop a scalable and rapid detection system using test strips and camera devices.
- Leverage machine learning models to create accurate predictive models.
- Enhance the solution's scalability while minimizing the need for trained human resources.

**Dataset Description:**
The dataset consists of 1,000 labeled images of milk test strips acquired under controlled conditions. Each image captures one or more test strips placed in a fixed geometric position, annotated to identify regions of interest (ROIs) where potential adulterants may be present. The dataset ensures consistency and reliability for developing and validating the detection algorithms.

**Methodology:**
1. **Data Collection:**
   - Images were acquired using high-resolution cameras under controlled lighting conditions to ensure consistency.
2. **Data Preprocessing:**
   - **K-means Segmentation:** Cropped images to focus on relevant sections, converted to grayscale, applied thresholding, and used K-means clustering for segmentation.
   - **Histogram-Based Thresholding:** Computed histograms to identify significant peaks and applied thresholds for image segmentation.
   - **Hue-Based Thresholding:** Converted images to HSV color space, applied thresholds to hue channel, and performed morphological operations to refine segmentation.
3. **Feature Extraction:**
   - Extracted features by converting images to different color spaces (RGB, HSV, LAB) and calculating average values for each channel. Categorized images based on specified thresholds.
4. **Model Selection and Training:**
   - Implemented Decision Tree, Random Forest, and XGBoost models.
   - Split dataset into training and testing sets (80-20 split) and used cross-validation for hyperparameter tuning.
   - Evaluated models using metrics like accuracy, precision, recall, and F1-score. XGBoost outperformed other models.
5. **Deployment:**
   - Developed a modular codebase using environment variables.
   - Containerized the application using Docker and deployed it on Azure.
   - Set up CI/CD pipelines with GitHub Actions for automated deployment.

**Results:**
The project successfully developed a machine learning-based system for detecting milk adulteration with high accuracy and reliability. The XGBoost model, in particular, demonstrated superior performance in terms of accuracy and balanced precision-recall metrics.

**Future Scope:**
- Quantifying the extent of adulteration in milk samples.
- Enhancing the system's integration with existing dairy industry workflows.
- Exploring additional machine learning models and image processing techniques to further improve detection accuracy.

**Conclusion:**
The AI-Powered Milk Adulteration Detection project provides a scalable, efficient, and cost-effective solution for detecting adulterants in milk. By leveraging machine learning and image processing techniques, the project contributes to enhancing food safety standards and consumer confidence in the dairy industry.

------
