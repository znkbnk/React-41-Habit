Step 1: Set Up State Variables

- Begin by declaring state variables using 
useState to keep track of the start and end dates.

Step 2: Reset Start and End Dates

- After successfully adding a habit, reset the
start and end dates to null.
- This ensures that each new habit starts with
a clean slate.

Step 3: Update Date Change Function

- Modify the function responsible for handling
date changes (handleDateChange).
- Check if a frequency is selected and a start
date is not set.
- If true, set the start date to the selected date.
- For weekly frequency, set the end date 7 days
after the start date.

Step 4: Create Tile Content Function

- Adjust the function responsible for displaying
content on each date tile (tileContent).
- If the selected frequency is weekly and start/end
dates are defined, show "Start" and "End"
buttons appropriately.

Step 5: Create handleFrequencyChange Function

- Create the function (handleFrequencyChange)
responsible for handling changes in the 
selected frequency.
- Reset both start and end dates to null when
the frequency changes.
- Make sure your dropdown menu for selecting
the frequency is correctly set up.

Step 6: Pass Tile Content to Calendar

- Ensure that the tileContent function is passed 
to the tileContent prop of the Calendar component.

Step 7: Set Goal Automatically for Weekly Habits

- Use the setEndDate function to update the state
variable responsible for storing the end date.
- Use the setHabit function to update both goalDays
and initialGoalDays to 7 for weekly frequency.

Step 8: Modify HabitList Component

- Update the display logic to verify if 
habit.selectedDateRange.start and 
habit.selectedDateRange.end are valid Date objects.
- You can use the instanceof operator to check
if a variable is an instance of the Date object.
- Modify the display logic to include an additional
check for valid Date objects.
- If they are valid Date objects, proceed with
displaying the date or date range. Otherwise,
handle it appropriately
(e.g., display a default value).

Step 9: Update useEffect in HabitList.js

- Check for variables that represent dates in string
format inside the useEffect block.
- Use the Date constructor or another appropriate
method to convert these date strings back to
Date objects.
- Apply Date Conversion to selectedDate:
If habit.selectedDate exists, create a new Date
object from the string; otherwise, set it to null.
- Apply Date Conversion to selectedDateRange:
If habit.selectedDateRange exists, create
new Date objects for start and end; otherwise,
set it to null.

Step 10: Create a Function to Determine Tile Classes

- Inside HabitForm.js file, create a function named
tileClassName. This function should take parameter date...
- Within the function, use conditional statements to
check if the date matches the start or end date.
If it does, return a specific class name
(e.g., "start-date-tile" or "end-date-tile").
- Define styles like background color and text color
for both "start-date-tile" and "end-date-tile" classes.
- When configuring the tileClassName prop of the
Calendar, use the tileClassName function to
dynamically assign classes to each date tile.



