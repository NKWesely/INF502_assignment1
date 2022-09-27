# Assignment 2: Python Basics

**Natasha Wesely**

**Sept 29, 2022**

Here's my link to my python file.

[Natasha's HW2 python code](code/INF502_HW2.py)


## Question 1

*1. Write a function with the following signature: pythagoreanTheorem(length_a, length_b).*

*The function returns the length of the hypotenuse assuming that length_a and length_b are the lengths of the two legs of a right triangle (the legs that form the triangle's right angle). Hint: the math module might have useful functions to use.*

```
# import the required modules
import math

def pythagoreanTheorem(length_a, length_b):
    # square length_a & length_b, add them together, then take the square root
    length_c = math.sqrt((length_a^2)+(length_b^2)) 
    # return the square root
    return length_c 

#Example Run 1
pythagoreanTheorem(1,2)
1.7320508075688772

#Example Run 2
pythagoreanTheorem(3,4)
2.6457513110645907

#Example Run 3
pythagoreanTheorem(9,9)
4.69041575982343

```

**Solution Approach Description:** I created a function that takes the arguments "length_a" and "length_b". The two lengths are squared individually, then added together. Then the square root of that value is taken, which is caluclated using the sqrt() function from the math module. The function then returns the square root as the hypotenuse.

## Question 2

*2. Write a function with the following signature: list_mangler(list_in).*

*The function assumes that list_in is a list of integers, and returns a new list containing transformed elements of list_in. If the element is even, it's doubled. If the element is odd, it's tripled.*

```

def list_mangler(list_in):
    list_out = [] # create an empty list for the output
    for i in list_in: # for each element in list_in
        if (i % 2) == 0: # if the element is even
             list_out.append(i*2) # double the element and append it to list_out
        else:
            list_out.append(i*3) # else, triple the element and append it to list_out
    return list_out 

#Example Run 1
list_mangler([2,4,6]) 
[4, 8, 12]

#Example Run 2
list_mangler([1,3,5])
[3, 9, 15]

#Example Run 3
list_mangler([1,9,6,14,21])
[3, 27, 12, 28, 63]

```

**Solution Approach Description:** I first created an empty list (“list_out”) that I could add elements to after performing the operations to the input elements. Then I created a for loop within my function that went through each element in the input list (“list_in”) and differentiated between odd and even numbers. If the element is divisible by 2 with a remainder of 0 (“if (i % 2) == 0”), then the element is even, and it gets doubled and then appended to the output list. If the element does not meet the conditional statement in the if clause, then it’s an odd number and it gets tripled and then appended to the output list. Finally, the function returns the output list.


## Question 3

*3. Write a function with the following signature: grade_calc(grades_in, to_drop).*

*The function accepts a list grades_in containing integer grades, drops the to_drop lowest grades (so, for to_drop equal to 2, the function should drop the 2 lowest grades), calculates the average of the grades left, and returns the letter grade this average corresponds to according to the letter grade scale for this course.*

```
# import needed modules
import statistics as st

def grade_calc(grades_in, to_drop=2):
    for i in grades_in:
        sort = sorted(grades_in) #sort the grades_in from lowest to highest
        del sort[:to_drop] #drop the values from the start of the list to number of grades to be dropped (to_drop)
        grade_avg = st.mean(sort) #find the mean of the remaining grades
        if (grade_avg >= 90): #if the avg grad is >= 90%
            return "A" #return the letter grade 'A'
        if (80 <= grade_avg > 90): #if the avg grad is between 80-90%
            return "B" #return the letter grade 'B'
        if (70 <= grade_avg > 80): #if the avg grad is between 70-80%
            return "C" #return the letter grade 'C'
        if (60 <= grade_avg > 70): #if the avg grad is between 60-70%
            return "D" #return the letter grade 'D'
        if (grade_avg < 60): #if the avg grad is < 60%
            return "F" #return the letter grade 'F'

#Example Run 1
grade_calc(grades_in=[90,95,98,100], to_drop=1)
'A'

#Example Run 2 using default to_drop=2
grade_calc(grades_in=[40,55,70,56,90,65,89])
'D'

#Example Run 3
grades= list(range(20,90))
grade_calc(grades_in=grades, to_drop=10)
'F'

```

**Solution Approach Description:** I created a for loop inside my function that goes through each element in the input list (“grades_in”). First the elements are sorted from lowest to highest. Then values are deleted from the sorted list based on how many grades need to be dropped (“to_drop”). Elements are deleted from index 0 to index “to_drop” (i.e., if to_drop=2, then the lowest two elements in the sorted list are deleted). Then the remaining elements in the sorted list are averaged. Then I have a series of if statements that evaluate the grade average and return the corresponding letter grade (i.e., if the average grade is >= 90% , the letter grade “A” is returned).

## Question 4

*4. Write a function with the following signature: odd_even_filter(numbers).*

*The function accepts an input list of integers and returns a list with two sublists. The first sublist contains all even numbers in the input list and the second sublist contains all odd numbers.*

```
def odd_even_filter(numbers):
    even_list = [] #create an empty list for the even values
    odd_list = [] #create an empty list for the odd values
    for i in numbers: #for each element in list "numbers"
        if i % 2==0: #if the element is even
            even_list.append(i) #append the even element to even_list
        else:
            odd_list.append(i) #else append the element to odd_list
                
        printlist = [even_list, odd_list] #create a list to print of the even_list and odd_list
    return(printlist) #return the print list

#Example Run 1
odd_even_filter(numbers= [6,7,8,9,10])
[[6, 8, 10], [7, 9]]

#Example Run 2
odd_even_filter(numbers= [5,7,2,2,4,6])

#Example Run 3
odd_even_filter(numbers= [7,7,7,7,7,7])

```

**Solution Approach Description:** First I created two empty lists, one for even numbers (“even_list”) and one for odd numbers (“odd_list”). Then I created a for loop that goes through each element in the input list (“numbers”). Within the for loop are two if statements. If the element is divisible by 2 with a remainder of 0 (“if (i % 2) == 0”), then the element is even, and it gets appended to the even_list. If the element does not meet the conditional statement in the if clause, then it’s an odd number and it gets appended to the odd_list. Then I created another list (“printlist”) that is a list of the even_list and odd_list. Finally, the “printlist” is returned.
