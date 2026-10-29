# FDS_LAB_2026
Day 1 Assignment 1
import numpy as np

# Marks matrix: 4 students × 5 subjects
rng = np.random.default_rng()
marks = rng.integers(0, 101, size=(4, 5))

# Calculate total marks for each student
total_marks = np.sum(marks, axis=1)

# Calculate percentage for each student
percentage = (total_marks / (5 * 100)) * 100

# Display results
print("Marks Matrix:")
print(marks)

print("\nTotal Marks of Each Student:")
print(total_marks)

print("\nPercentage of Each Student:")
print(percentage)

# Calculate average marks for each subject
average_marks = np.mean(marks, axis=0)

# Calculate standard deviation for each subject
std_deviation = np.std(marks, axis=0)

# Display results
print("Marks Matrix (4 Students × 5 Subjects):")
print(marks)

print("\nAverage Marks in Each Subject:")
print(average_marks)

print("\nStandard Deviation in Each Subject:")
print(std_deviation)



import numpy as np

# Generate marks for 4 students in 5 subjects
rng = np.random.default_rng()
marks = rng.integers(0, 101, size=(4, 5))

# Find the highest marks in each subject
highest_marks = np.max(marks, axis=0)

# Find the index of the student who scored the highest marks
student_index = np.argmax(marks, axis=0)

# Display results
print("Marks Matrix (4 Students × 5 Subjects):")
print(marks)

print("\nHighest Marks in Each Subject:")
print(highest_marks)

print("\nIndex of Student Scoring Highest Marks in Each Subject:")
print(student_index)

print("\nStudent Number (1-based indexing):")
print(student_index + 1)

import numpy as np

# Generate marks for 4 students in 5 subjects
rng = np.random.default_rng()
marks = rng.integers(0, 101, size=(4, 5))

# Create a Boolean mask: True for Pass, False for Fail
pass_mask = marks >= 40

# Display results
print("Marks Matrix (4 Students × 5 Subjects):")
print(marks)

print("\nBoolean Mask (True = Pass, False = Fail):")
print(pass_mask)

# Display Pass/Fail status
print("\nPass/Fail Status:")
print(np.where(pass_mask, "Pass", "Fail"))
