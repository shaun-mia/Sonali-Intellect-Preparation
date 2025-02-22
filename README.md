---

# **📌 Python & SQL Written Exam – Questions & Answers**

## **🔹 Python (Basic to Advanced)**  

### **1️⃣ Basics of Python**  
**Q1. What is indentation in Python, and why is it important?**  
👉 **Answer:** Indentation refers to spaces or tabs used at the beginning of code lines to define a block of code (like loops, conditions, functions). Unlike other languages, Python relies on indentation instead of curly braces `{}` for structuring the code.

---

**Q2. Explain the difference between `=` and `==` in Python.**  
👉 **Answer:**  
- `=` is an **assignment operator** used to assign a value to a variable (e.g., `x = 5`).  
- `==` is a **comparison operator** used to check equality (e.g., `if x == 5:`).  

---

**Q3. What are the different data types in Python? Provide examples.**  
👉 **Answer:**  
- `int` → `x = 10`  
- `float` → `y = 10.5`  
- `str` → `name = "John"`  
- `bool` → `is_valid = True`  
- `list` → `arr = [1, 2, 3]`  
- `tuple` → `tup = (1, 2, 3)`  
- `set` → `s = {1, 2, 3}`  
- `dict` → `d = {"name": "John", "age": 25}`  

---

**Q4. What is the output of the following code?**  
```python
x = 5
y = "5"
print(x + int(y))
```
👉 **Answer:** `10`  
(`int(y)` converts `"5"` to `5`, so `5 + 5 = 10`).

---

**Q5. Write a Python program to check if a number is even or odd.**  
```python
num = int(input("Enter a number: "))
if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

### **2️⃣ Control Statements**  
**Q6. What is the difference between `break`, `continue`, and `pass`?**  
👉 **Answer:**  
- `break` → Exits the loop completely.  
- `continue` → Skips the current iteration and continues the next one.  
- `pass` → Placeholder that does nothing (used when a statement is required syntactically).  

---

**Q7. Write a program to print numbers from 1 to 10 using a `for` loop.**  
```python
for i in range(1, 11):
    print(i)
```

---

**Q8. How does a `while` loop work? Write a program to find the sum of digits of a number.**  
```python
num = int(input("Enter a number: "))
sum_digits = 0
while num > 0:
    sum_digits += num % 10
    num //= 10
print("Sum of digits:", sum_digits)
```

---

### **3️⃣ Functions**  
**Q9. What are `*args` and `**kwargs` in Python functions?**  
👉 **Answer:**  
- `*args` → Allows a function to accept multiple positional arguments.  
- `**kwargs` → Allows a function to accept multiple keyword arguments.  

Example:  
```python
def test_func(*args, **kwargs):
    print(args)  # Tuple of arguments
    print(kwargs)  # Dictionary of keyword arguments

test_func(1, 2, 3, name="John", age=25)
```

---

**Q10. Write a function to find the factorial of a number using recursion.**  
```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```

---

### **4️⃣ Data Structures (Lists, Tuples, Sets, Dictionaries)**  
**Q11. How do lists differ from tuples in Python?**  
👉 **Answer:**  
- **Lists** are mutable (`[1, 2, 3]`) → Elements can be modified.  
- **Tuples** are immutable (`(1, 2, 3)`) → Elements cannot be changed.  

---

**Q12. Write a list comprehension to create a list of squares of numbers from 1 to 10.**  
```python
squares = [x**2 for x in range(1, 11)]
print(squares)
```

---

**Q13. How can you remove duplicate elements from a list?**  
👉 **Answer:**  
```python
lst = [1, 2, 2, 3, 4, 4, 5]
unique_lst = list(set(lst))
print(unique_lst)  # Output: [1, 2, 3, 4, 5]
```

---

### **5️⃣ Object-Oriented Programming (OOP)**  
**Q14. What is encapsulation? Provide an example.**  
👉 **Answer:** Encapsulation restricts access to certain variables/methods in a class.  

Example:  
```python
class Car:
    def __init__(self, brand):
        self.__brand = brand  # Private variable

    def get_brand(self):
        return self.__brand

car = Car("Toyota")
print(car.get_brand())  # Output: Toyota
```

---

**Q15. Explain inheritance in Python with an example.**  
👉 **Answer:** Inheritance allows a child class to inherit properties from a parent class.  

Example:  
```python
class Animal:
    def speak(self):
        return "Animal speaks"

class Dog(Animal):
    def speak(self):
        return "Bark"

dog = Dog()
print(dog.speak())  # Output: Bark
```

---

## **🔹 SQL (Basic to Advanced)**  

### **1️⃣ Basics of SQL**  
**Q16. What are the differences between `DDL` and `DML` commands? Provide examples.**  
👉 **Answer:**  
- `DDL` (Data Definition Language) → Defines structure (`CREATE`, `ALTER`, `DROP`).  
- `DML` (Data Manipulation Language) → Manipulates data (`INSERT`, `UPDATE`, `DELETE`).  

---

**Q17. Write an SQL query to create a table named `employees`.**  
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    salary DECIMAL(10,2)
);
```

---

**Q18. Write an SQL query to retrieve employees with salaries greater than 50,000.**  
```sql
SELECT * FROM employees WHERE salary > 50000;
```

---

### **2️⃣ Intermediate SQL**  
**Q19. Explain different types of SQL joins.**  
👉 **Answer:**  
- `INNER JOIN` → Returns matching records from both tables.  
- `LEFT JOIN` → Returns all records from the left table and matching ones from the right.  
- `RIGHT JOIN` → Returns all records from the right table and matching ones from the left.  
- `FULL JOIN` → Returns all records from both tables.  

---

### **3️⃣ Advanced SQL**  
**Q20. Write an SQL query to find the second highest salary in a table.**  
```sql
SELECT MAX(salary) 
FROM employees 
WHERE salary < (SELECT MAX(salary) FROM employees);
```

---

# **📌 Final Tips**
✅ **Practice Python scripts & SQL queries daily**  
✅ **Focus on real-world scenarios & problem-solving**  
✅ **Understand SQL execution flow & Python OOP concepts**  
