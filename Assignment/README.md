# Jake Fraser

##Lab Exercise 1: Introduction to C, Git, and the MSP430

## Function
This program will take in two numbers as inputs and perform a specified operation decided on by the user. Future applications of a program such as this include personal calculators, data manipulation, and automation. Eventually this prgram will be paired with a development bard to create a functinal UART calculator. 

##Usage
In order to properly use this program, three files will be needed, and can all be found in this repository. The header file, math.h, defines the set function declarations and headers used in this program. It is absolutely necessary in running the code so that the program knows what each function is.
The next file, math.c, contains the most important part of this program. This is where the program takes in its inputs, computes the necessary functions, and sends out the desired output. The last file used to run this program is the main.c file. This is what is actually ran by the user in order to complete the desired function. Depending on what they, the user will input the desired variables here. These variables can be entered in the apprpriate spaces in line 5 of the main.c code. This layout can be seen below.

int sum = math(num1,num2,'operator') ;

For example, if the user wanted to multiply the integers 4 and 5, they would enter the following line of code into line 5. 

int sum = math(4,5,'*') ;

The list of available functions is as follows:
 * + Add (num1 + num2)
 * - Subtract (num1 - num2)
 * * Multiply (num1 * num2)
 * / Divide (num1 / num2)
 * % Modulus (num1 % num2)

##Variables 
There are three main variables defined in this program that the user will interact with. The first two, labeled as num1 and num2, are the integers that the user wants to perform operations on. It is very important that these numbers are integers and not doubles, as a decimal will not be understood in this program. The final variable is a character. This character is defined by the user and is used to determine what operation will be used. Available operations can be found above. 

##How it works
The math.c uses a series of if statements to determine which operation to perform on the two integers to select. If a "+" sign is selected, then the two integers will be added together. If a "-" sign is selected, then num2 will be subtracted from num1. When a "*" is selected, the two integers will be multiplied. A "/" sign signifies that the num1 will be divided by num2. And finally, "%" indicates that a modulus between the two numbers will be taken. In order to ensure that the program runs even without an appropriate variable, it will display -1 in the case where no apprpriate character is selected. 
