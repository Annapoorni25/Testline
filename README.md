# Testline
# Project Overview
This project will take a quiz dataset, summarize performance per topic, and provide actionable recommendations for improvement. It identifies weak areas based on response accuracy to aid in prioritizing topics that require more attention.

# Installation Steps
Download or clone the project repository to your local machine.
Install the necessary library by executing:
            pip install pandas
Prepare Dataset: 
            Save your dataset as quizdataset.csv.
            Place it in the Your comfortable directory
            Run the script in your Python environment:
                    python script_name.py
            Replace script_name.py with the name of your script file.
Review Output:
            The console output will print a quick summary.
            Detailed results will be saved to:
                    topicsummary.csv
                    recommendations.csv

# Approach Description
  # 1.Data Cleaning
        Filter dataset to retain only the relevant columns: id, topic, difficulty_level, and correctness of options.
        Filled missing values for difficulty_level with "Unknown".
  # 2.Calculation of Performance
      Sum correct responses per question by adding correctness values from the option columns.
      Grouped data by topic and difficulty_level to calculate:
          Total questions in each group.
          Average number of correct responses.
  # 3.Weak Topics Identification
      Topics whose average count of correct responses is less than 1.5 are weak.
      Saves weak topics to a separate CSV for further action.
  # 4.Generating Recommendations
      Defines thresholds for recommendations based on the average correct count:
          <1.0: Revise thoroughly.
            1.0 - 1.5: Practice more.
              >1.5: Maintain current performance.
  # 5. Output Generation
      Exports:
          topicsummary.csv: Comprehensive performance analysis.
          recommendations.csv: Insights for weak topics.
