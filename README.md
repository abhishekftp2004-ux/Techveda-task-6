# Task 6: List and Dictionary Comprehensions

# 1. Basic list comprehension
numbers = list(range(1, 11))
squares = [n**2 for n in numbers]
print("Squares:", squares)

# 2. Filtering
even_numbers = [n for n in numbers if n % 2 == 0]
odd_numbers = [n for n in numbers if n % 2 != 0]
print("Even:", even_numbers)
print("Odd:", odd_numbers)

# 3. Transformation
names = ["rahul", "priya", "aman", "neha"]
uppercase_names = [name.upper() for name in names]
name_lengths = [len(name) for name in names]
print("Uppercase:", uppercase_names)
print("Lengths:", name_lengths)

# 4. Student marks
marks = [85, 92, 67, 76, 55, 88, 72]
passed_marks = [m for m in marks if m >= 60]
grades = ["A" if m >= 80 else "B" if m >= 60 else "C" for m in marks]
print("Passed:", passed_marks)
print("Grades:", grades)

# 5. Nested list comprehension
matrix = [[1,2,3],[4,5,6],[7,8,9]]
flattened = [x for row in matrix for x in row]
print("Flattened:", flattened)

# 6. Dictionary comprehension
square_dict = {n: n**2 for n in range(1, 6)}
print("Squares dictionary:", square_dict)

# 7. Student dictionary comprehension
students = {"Rahul":85, "Priya":92, "Aman":67, "Neha":76, "Rohit":55}
student_grades = {
    name: ("A" if mark >= 80 else "B" if mark >= 60 else "C")
    for name, mark in students.items()
}
top_students = {name: mark for name, mark in students.items() if mark >= 80}
print("Grades:", student_grades)
print("Top students:", top_students)

# 8. Product transformation and filtering
products = {"Laptop":65000, "Phone":30000, "Headphones":2500,
            "Keyboard":1800, "Monitor":15000}
discounted = {p: round(price*0.90, 2) for p, price in products.items()}
premium = {p: price for p, price in products.items() if price >= 10000}
print("Discounted:", discounted)
print("Premium:", premium)

# 9. Traditional loop vs comprehension
loop_result = []
for n in numbers:
    if n % 2 == 0:
        loop_result.append(n**2)
comprehension_result = [n**2 for n in numbers if n % 2 == 0]
print("Loop:", loop_result)
print("Comprehension:", comprehension_result)
print("Same result:", loop_result == comprehension_result)

# 10. Practical student records
records = [
    {"name":"Rahul", "marks":85},
    {"name":"Priya", "marks":92},
    {"name":"Aman", "marks":67},
    {"name":"Neha", "marks":76},
    {"name":"Rohit", "marks":55}
]
passed_students = [r["name"] for r in records if r["marks"] >= 60]
score_dict = {r["name"]: r["marks"] for r in records}
print("Passed students:", passed_students)
print("Score dictionary:", score_dict)
