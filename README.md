Workbook Structure
1. NEW DAY Sheet
Purpose: The "NEW DAY" sheet is where you input the data for your current workout session.

Columns:

Muscle Group: Shows the muscle group associated with the exercise (e.g., Back, Chest, Legs).
Exercise: Lists the exercises you'll perform in your workout (e.g., Bicep Curl, Squat).
Last Time (Weight): Shows the weight you used the last time you performed this exercise.
Last Time (Reps): Shows the number of reps you completed the last time for this exercise.
Comment: Displays any notes you added the last time, like "Felt strong" or "Reduce weight next time."
New Weight (kg): Where you input the weight you are using for the current session.
New Reps: Where you input the number of reps completed for the current session.
New Comments: Add any new comments or observations about this exercise session.
How it works:

The workbook automatically references the previous performance data (last weight and reps) from the RECORD sheet to guide your current workout.
After completing your workout, a macro will transfer the new data (weight, reps, comments) to the corresponding row in the RECORD sheet, preserving your historical data and allowing you to track your progress.
2. RECORD Sheet
Purpose: The "RECORD" sheet stores the historical data for each exercise. It logs your performance for every session, including date, weight, reps, and any comments.
Columns:
Exercise: Lists all exercises you track.
Date: The date of each session in which the exercise was performed.
Weight (kg): The amount of weight lifted during that session.
Reps: The number of repetitions completed for that session.
Comments: Any additional observations from that workout session.
How it works:
Each exercise in the "NEW DAY" sheet corresponds to a row in the "RECORD" sheet. As you log your workout data, the macro will append the latest information (date, weight, reps, comments) to the next available column in the correct row for each exercise.
This keeps a continuous log of your progress, which you can review at any time.
How to Use This Workbook
Input Your New Workout in NEW DAY:

Go to the "NEW DAY" sheet.
Enter the weight and reps for each exercise you perform in the "New Weight (kg)" and "New Reps" columns.
Add any comments you want to track in the "New Comments" column.
Run the Macro:

After entering all your workout data, run the macro by clicking the "New Day" button (if you have created a button for it).
The macro will:
Transfer the current workout data into the RECORD sheet, adding the new data to the history.
Clear the "New Weight", "New Reps", and "New Comments" columns in the "NEW DAY" sheet to prepare it for the next session.
Review Your Progress:

In the "RECORD" sheet, you can review the historical data for each exercise, including the weights lifted and reps completed in previous sessions.
Macro Explanation
The macro automates the transfer of data from the NEW DAY sheet to the RECORD sheet. Here's what the macro does:

Data Check: It checks the "New Weight" and "New Reps" columns to ensure you've input values.
Data Transfer: For each exercise where you've entered data, the macro finds the corresponding row in the RECORD sheet and adds a new entry with the current date, weight, reps, and comments.
Data Clearing: After transferring the data, the macro clears the input columns (New Weight, New Reps, New Comments) in the "NEW DAY" sheet so you can start fresh the next time.
Tips for Best Use
Regularly Review Historical Data: Use the RECORD sheet to observe patterns in your performance. This can help you understand where you’re improving and where you may need to adjust your training.
Consistent Input: Make sure to always input the new weight and reps data for each exercise. This ensures that the macro accurately logs your progress over time.
Add Comments: Don’t hesitate to add comments after each session. It’s a great way to capture qualitative data like how you felt during the workout or any specific adjustments you made.
Troubleshooting
Macro Errors: If the macro fails, ensure that all necessary fields (New Weight and New Reps) are filled before running it.
Clearing Data: Be cautious when manually clearing cells. The macro already clears the input fields for you after a new workout is logged.