# Simple-calculator
def calculate_grade(marks):
    total = sum(marks)
    average = total / len(marks)

    # Control flow: determine grade based on average
    if average >= 90:
        grade = "A+"
    elif average >= 80:
        grade = "A"
    elif average >= 70:
        grade = "B"
    elif average >= 60:
        grade = "C"
    elif average >= 50:
        grade = "D"
    else:
        grade = "F"

    return total, average, grade


# Get marks for 5 subjects
marks = []

for i in range(1, 6):
    while True:
        mark = float(input(f"Enter marks for subject {i}: "))

        # Control flow: validate marks
        if 0 <= mark <= 100:
            marks.append(mark)
            break
        else:
            print("Invalid marks. Enter a value between 0 and 100.")

# Calculate result
total, average, grade = calculate_grade(marks)

# Display result
print("\n----- RESULT -----")
print("Total Marks:", total)
print("Average:", round(average, 2))
print("Grade:", grade)
