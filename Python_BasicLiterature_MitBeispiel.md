# i can comment with pound sign . yes, that's also comment

# Assigning string to a variable
a = "This is a string"
print(a)
#The output is : This is string


# Declaring a list
L = [1, "a" , "string" ,3]
print L
#The output is:
[1, 'a', 'string', 3]

# Tuples in Python
tup = (1,2,3,4)
print (tup)
#The output is (1,2,3,4) #Tuples are like lists but they cannot be changed.

#Python Operators

  #Arithmetic Operators
  + 	Addition:	x + y
  - 	Subtraction: 	x - y
  * 	Multiplication: 	x * y
  / 	Division (float):	x / y
  % 	Modulus:  x % y
  ** 	Power :  	x ** y

  # Relational Operators
  > 	Greater than:  	x > y
  <  Less than: 	x < y
  == Equal to:	x == y
  != 	Not equal to : 	x != y
  >= 	Greater than or equal to:	x >= y
  <= 	Less than or equal to:  	x <= y

  # Logical operators
  and Logical AND: True if both the operands are true 	x and y
  or 	Logical OR: True if either of the operands is true 	x or y
  not Logical NOT: True if operand is false 	not x


# python program to illustrate If statement
i = 10
if (i < 15):
   print ("10 is less than 15")
#The output is : 10 is less than 15


#if- else
# if we want to do something else if the condition is false.
i = 20;
if (i < 15):
    print ("i is smaller than 15")
    print ("i'm in if Block")
else:
    print ("i is greater than 15")
#The output is : i is greater than 15


#if-elif-else ladder
#Here,you can decide among multiple options
i = 20
if (i == 10):
    print ("i is 10")
elif (i == 15):
    print ("i is 15")
elif (i == 20):
    print ("i is 20")
else:
    print ("i is not present")

#The output is : i is 20


#Iterations in Python
#Iteration by while loop for a condition
i = 1
while (i < 10):
    i += 1
    print i,
#The output is : 2 3 4 5 6 7 8 9 10


#Iteration by for loop on list
L = [1, 4, 5, 7, 8, 9]
for  i in L:
    print i,
#The output is : 1 4 5 7 8 9



# We can create our own functions!
# A simple Python function to check
# whether x is even or odd
def evenOdd( x ):
    if (x % 2 == 0):
        print "even"
    else:
        print "odd"
# Driver code
  evenOdd(3)
# Output is : odd
