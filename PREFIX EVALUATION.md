# Exp.No:34  
## PREFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.

---

### ALGORITHM

1. **Start the program.**
2. Define a set of valid operators: `*, -, +, %, /, **`.
3. Initialize an empty stack.
4. Traverse the prefix expression from **right to left**:
   - If the character is a **digit**, convert it to an integer and push it onto the stack.
   - If the character is an **operator**, pop two elements from the stack.
     - Apply the operator on the two popped operands.
     - Push the result back onto the stack.
   - If an invalid character is encountered, raise an error.
5. After traversal, the stack should contain only **one element**.
6. Return the **single element** as the evaluation result.
7. **End the program.**

---

### PROGRAM
```
OPERATORS = set(['*', '-', '+', '%', '/', '**']) 
def evaluate(expression):
    stack = []
    for symbol in reversed(expression):
        if symbol not in OPERATORS:
            stack.append(int(symbol))  
        else:
            operand1 = stack.pop()
            operand2 = stack.pop()
            if symbol == '+':
                stack.append(operand1 + operand2)
            elif symbol == '-':
                stack.append(operand1 - operand2)
            elif symbol == '*':
                stack.append(operand1 * operand2)
            elif symbol == '/':
                stack.append(operand1 // operand2) 
            elif symbol == '%':
                stack.append(operand1 % operand2)
            elif symbol == '**':
                stack.append(operand1 ** operand2)
    return stack.pop()
test_expression = input()
print("Prefix Expression :", test_expression)
print("Evaluation result :", evaluate(test_expression))
```
### OUTPUT

<img width="825" height="260" alt="Screenshot 2025-09-10 082432" src="https://github.com/user-attachments/assets/8bdd1b38-8513-4aaf-b6eb-738d1af5d5ee" />

### RESULT

Thus, the python code is written and executed successfully.
