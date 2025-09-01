# Netflix Movie Data Analysis: Trends, Popularity, and Genre Insights

## 📖 Overview

This repository contains a comprehensive data analysis of a movie dataset from a CSV file named `mymoviedb.csv`. The project walks through the entire data analysis process, from cleaning and preprocessing the data to exploratory data analysis (EDA) and visualization. The goal is to uncover insights into movie trends, identify popular genres, and understand the factors contributing to a movie's success.


## 💾 Dataset

[cite_start]The dataset used for this analysis is `mymoviedb.csv` [cite: 5][cite_start], which contains information about 9,827 movies[cite: 11]. The key columns in the dataset include:

* [cite_start]**Title**: The title of the movie[cite: 6].
* [cite_start]**Release_Date**: The release date of the movie[cite: 6].
* [cite_start]**Genre**: The genre(s) associated with the movie[cite: 6].
* [cite_start]**Popularity**: A score representing the movie's popularity[cite: 6].
* [cite_start]**Vote_Average**: The average user rating[cite: 6].
* [cite_start]**Vote_Count**: The total number of votes received[cite: 6].

## ⚙️ Analysis and Methodology

The analysis was conducted in a step-by-step manner to ensure the data was clean, organized, and ready for visualization.

### 1. **Data Cleaning and Preprocessing**

* **Initial Inspection**: The dataset was loaded and inspected for null values and duplicates. [cite_start]The data was found to be clean with no missing or duplicated rows[cite: 14, 16].
* [cite_start]**Data Type Conversion**: The `Release_Date` column was converted from an `object` to a `datetime` format, and then the year was extracted into a new integer column[cite: 57, 60].
* [cite_start]**Dropping Unnecessary Columns**: The `Poster_Url`, `Overview`, and `Original Language` columns were dropped as they were not required for this analysis[cite: 70].
* **Handling Categorical Data**:
    * [cite_start]The `Genre` column, which contained multiple comma-separated values, was split and exploded so that each movie-genre pair occupied a single row[cite: 124, 125].
    * [cite_start]The `Vote_Average` was categorized into four distinct groups: **'not_popular'**, **'below_avg'**, **'average'**, and **'popular'** based on its statistical distribution (min, 25%, 50%, 75%, max)[cite: 78, 83].

### 2. **Exploratory Data Analysis (EDA) and Visualization**

The cleaned data was visualized to answer key questions about the movie dataset.

#### Key Questions Addressed:
1.  **What is the most frequent genre of movies?**
    * [cite_start]**Finding**: **Drama** is the most frequent genre, followed by Comedy and Action[cite: 158].
    
2.  **What movie has the highest and lowest popularity?**
    * [cite_start]**Finding (Highest)**: **'Spider-Man: No Way Home'** has the highest popularity score of 5083.954[cite: 205, 208]. [cite_start]Its genres are Action, Adventure, and Science Fiction[cite: 208].
    * [cite_start]**Finding (Lowest)**: **'The United States vs. Billie Holiday'** and **'Threads'** share the lowest popularity score of 13.354[cite: 211, 213].

3.  **Which year saw the most movie releases?**
    * [cite_start]**Finding**: The number of movies released has significantly increased over time, with a major spike in the years leading up to **2020**[cite: 218, 232].
    
## 🛠️ Tools and Libraries Used

The analysis was performed using Python and the following libraries:

* [cite_start]**pandas**: For data manipulation and analysis[cite: 1].
* [cite_start]**NumPy**: For numerical operations[cite: 2].
* [cite_start]**Matplotlib**: For creating static and interactive visualizations[cite: 3].
* [cite_start]**Seaborn**: For high-level statistical data visualization[cite: 4].

## 🚀 How to Run This Project

To replicate this analysis, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd your-repository-name
    ```
3.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
4.  **Run the Jupyter Notebook or Python script.**

Make sure the `mymoviedb.csv` file is in the same directory as your script or notebook.
