# Python-Project-file
Python program to check whether the given number(s) is/are fibonacci or not.
# Creating an empty list to get the terms to be checked
user_list= [ ]

# Asking the user number of terms that are to be checked
terms= int (input( ' enter the number of terms you want to check ' ))

# Using 'for' loop to append the terms in the user_list
for i in range (terms) :
    print('enter the' ,i+1 ,' number', end='    ')
    num= int(input())
    user_list.append(num)
print()
print()

# Using 'max()' function to get the highest number user has input
max_num= max(user_list)

# Initializing first two fibonacci terms in a list
fib_list = [0, 1]  

# Setting the upper limit to make the list of fibonacci terms using         #max_num
while fib_list[-1] <= max_num:
    
    # Adding new fibonacci terms until the max_num is reached
    fib_list.append(fib_list[-1] + fib_list[-2])
    
# Checking whether 'user_list' is/are 'in' the list of 'fib_list' using 'for' loop
# Printing whether the given number(s) is/are valid fibonacci numbers(s) #or not

for j in range (terms):
    if user_list[j] in fib_list :
        print(user_list[j],'  is valid')
    else:
        print(user_list[j],'  is invalid')

