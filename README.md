# Basic Calculator

def add(n1,n2):
  return n1+n2

def sub(n1,n2):
  return n1-n2
  
def mul(n1,n2):
  return n1*n2
  
def div(n1,n2):
  if n2==0:
    return "$"
  else:
    return n1/n2

print("--- Basic Calculator ---")
print("1. Addition\n2. Substraction\n3. Multiplication\n4. Division")
opt = int(input("Enter any option [1,2,3,4]: "))

if opt not in [1,2,3,4]:
  print("Invalid Input!")
else:
  num1 = float(input("Enter the first number: "))
  num2 = float(input("Enter the second number: "))
  
  if opt==1:
    print(f"Addition Result: {add(num1,num2)}")
  elif opt==2:
    print(f"Substraction Result: {sub(num1,num2)}")
  elif opt==3:
    print(f"Multiplication Result: {mul(num1,num2)}")
  elif opt==4:
    if div(num1,num2)=="$":
      print("Cannot Divide by Zero")
    else:
      print(f"Division Result: {div(num1,num2)}")
