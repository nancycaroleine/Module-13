# Exp.No:33  
## POSTFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.

---

### ALGORITHM

1. **Start the program.**
2. Define a set named `OPERATORS` containing all the valid operators: `*, +, **, -, /, %`.
3. Define a function `evaluate_postfix(exp)` to evaluate the postfix expression:
   - Inside the function, create an empty list called `stack` to store operands and intermediate results.
4. Loop through each item in the given postfix expression:
   - If the current item is **not in OPERATORS**, it is an operand, so append it to the stack.
   - If the current item is an **operator**:
     - Pop the top two elements from the stack (first pop is `a`, second pop is `b`).
     - Perform the operation `b <operator> a` depending on the current operator.
     - Store the result in a variable called `result`.
     - Append the result back to the stack.
5. After the loop ends, return the first element of the stack as the final evaluation result.
6. Take a postfix expression as input from the user.
7. Print the postfix expression.
8. Call the function `evaluate_postfix()` with the input and print the result.
9. **End the program.**

---

### PROGRAM
```
OPERATORS=set(['*','+','/'])

def string_conv(str):
    l=[]
    for i in range(0,len(str)):
        if(str[i].isdigit() and str[i+1].isdigit()):
            st=str[i]+str[i+1]
            l.append(st)
        elif(str[i] in OPERATORS):
            l.append(str[i])
    
    return l;



def evaluate_postfix(expression):
    exp=string_conv(expression)
    stack=[]
    for i in exp:
        if i not in OPERATORS:
            stack.append(i)  
        
        else:
            a=stack.pop()  
            b=stack.pop()
        
            if i=='+':
                res=int(b)+int(a)  
              
            elif i=='*':
                res=int(b)*int(a)
            
            elif i=='/':
                res=int(b)/int(a)
            
            stack.append(res) 
    return stack[0]
expression = input()
print('postfix expression: ',expression)
print('Evaluation result: ',evaluate_postfix(expression))
```
### OUTPUT

<img width="577" height="150" alt="image" src="https://github.com/user-attachments/assets/b96d4785-26c0-4ee1-be93-75dd5158dfe8" />

### RESULT

Thus, the python code is written and executed successfully.
