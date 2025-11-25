# Exp.No:31  
## IMPLEMENTATION OF STACK

---

### AIM  
To write a Python program to implement a stack using a list and its built-in methods (`append()`, `pop()`).

---

### ALGORITHM

1. **Start the program.**
2. **Define a class `st`** with the following methods:
   - `push(self, num)`: Adds the number `num` to the stack.
   - `pop(self)`: Removes and returns the top element from the stack.
3. **Create a stack object `s`** using the class `st`.
4. **Input the stack size**: Take an integer input `size` to define the size of the stack.
5. **Loop through numbers from 1 to size**: Add only the odd numbers to the stack using the `push()` method.
6. **Display the elements** in the stack after the loop completes.
7. **Call `pop()`** to remove the top element from the stack and display the popped element.
8. **Display the stack again** to show the remaining elements.
9. **End the program.**

---

### PROGRAM
```
OPERATORS=set(['*','+']) 
def evaluate_postfix(expression):
    stack=[]
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)
        else:
            a = stack.pop()
            b = stack.pop()
            if i == '+':
                res = int(b)+int(a)
            elif i == '*':
                res = int(b) * int(a)
            stack.append(res)
    return stack[0]        
expression = input()
print("postfix expression: ", expression)
print("Evaluation result: ", evaluate_postfix(expression))
```
### OUTPUT

<img width="821" height="193" alt="image" src="https://github.com/user-attachments/assets/5490b252-5743-4988-9207-1067061e3b5b" />

### RESULT

Thus, the python code is written and executed successfully.
