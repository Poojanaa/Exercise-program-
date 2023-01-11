**1. C++ program to implement singly linked list**<br>
#include <iostream><br>
#include<cstdlib><br>
using namespace std;<br>
struct Node {<br>
   int data;<br>
   struct Node *next;<br>
};<br>
struct Node* head = NULL;<br>
void insert(int new_data) {<br>
   struct Node* new_node = (struct Node*) malloc(sizeof(struct Node));<br>
   new_node->data = new_data;<br>
   new_node->next = head;<br>
   head = new_node;<br>
}<br>
void display() {<br>
   struct Node* ptr;<br>
   ptr = head;<br>
   while (ptr != NULL) {<br>
      cout<< ptr->data <<" ";<br>
      ptr = ptr->next;<br>
   }<br>
}<br>
int main() {<br>
   insert(3);<br>
   insert(1);<br>
   insert(7);<br>
   insert(2);<br>
   insert(9);<br>
   cout<<"The linked list is: ";<br>
   display();<br>
   return 0;<br>
}<br>
<br>
<br>
  **Output:-**<br>
  The linked list is: 9 2 7 1 3<br>
  --------------------------------<br>
	<br>
	<br>
   **2. C++ program to implement insertion and deletion node in front position**<br>
   #include<iostream><br>
#include<cstdlib><br>
using namespace std;<br>
struct node<br>
{<br>
	int info;<br>
	struct node *next;<br>
}*start;<br>
class single_llist<br>
{<br>
	public:<br>
	node* create_node(int);<br>
	void insert_begin();<br>
	void delete_begin();<br>
	void display();<br>
	single_llist()<br>
	{<br>
		start=NULL;<br>
		
	}<br>
};<br>
int main()<br>
{<br>
	int choice;<br>
	single_llist s1,s2;<br>
	start=NULL;<br>
	do<br>
	{<br>
		cout<<"__________"<<endl;<br>
		cout<<"Operations on singly linked list"<<endl;<br>
		cout<<"__________"<<endl;<br>
		cout<<"1.Insert at first"<<endl;<br>
		cout<<"2.Delete at first"<<endl;<br>
		cout<<"3.Display"<<endl;<br>
		cout<<"4.Exit"<<endl;<br>
		cout<<"Enter your choice:";<br>
		cin>>choice;<br>
		switch(choice)<br>
		{<br>
			case 1:s1.insert_begin();<br>
			s1.display();<br>
			break;<br>
			case 2:s2.delete_begin();<br>
			s1.display();<br>
			break;<br>
			case 3:s1.display();<br>
			break;<br>
			case 4:exit(0);<br>
			break;<br>
			default:cout<<"Wrong choice....???"<<endl;<br>
			break;<br>
		}<br>
	}<br>
	while(choice !=4);<br>
}<br>
node *single_llist::create_node(int value)<br>
{<br>
 struct node *temp, *s; <br>
 temp = new(struct node); <br>
 if (temp == NULL) <br>
 { <br>
   cout<<"Memory not allocated"<<endl; <br>
 return 0; <br>
 } <br>
 else <br>
 { <br>
 temp->info = value; <br>
 temp->next = NULL; <br>
 return temp; <br>
 } <br>
	 
}<br>
void single_llist::insert_begin() <br>
{ <br>
 int value; <br>
 cout<<"Enter the value to be inserted : "; <br>
 cin>>value; <br>
 struct node *temp, *s; <br>
 temp = create_node(value); <br>
 if (start == NULL) <br>
 { <br>
 start = temp; <br>
 start->next = NULL; <br>
 cout<<temp->info<<" is inserted at first in the empty list"<<endl; <br>
 } <br>
 else <br>
 { <br>
 s = start; <br>
 start = temp; <br>
 start->next = s; <br>
 cout<<temp->info<<" is inserted at first"<<endl; <br>
 } <br>
} <br>
void single_llist::delete_begin() <br>
{ <br>
 if (start == NULL){} <br>
 else <br>
 { <br>
 struct node *s, *ptr; <br>
 s = start; <br>
 start = s->next; <br>
 cout<<s->info<<" deleted from first"<<endl; <br>
 free(s); <br>
 } <br>
} <br>
void single_llist::display() <br>
{ <br>
 struct node *temp; <br>
 if (start == NULL) <br>
 cout<<"Linked list is empty...!!!"<<endl; <br>
 else <br>
 { <br>
 cout<<"Linked list contains : "; <br>
 temp = start; <br>
 while (temp != NULL) <br>
 { <br>
 cout<<temp->info<<" "; <br>
 temp = temp->next; <br>
 } <br>
 cout<<endl; <br>
 } <br>
}<br>
<br>
<br>
**Output:-**<br>
   __________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:1<br>
Enter the value to be inserted : 10<br>
10 is inserted at first in the empty list<br>
Linked list contains : 10<br>
__________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:1<br>
Enter the value to be inserted : 20<br>
20 is inserted at first<br>
Linked list contains : 20 10<br>
__________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:1<br>
Enter the value to be inserted : 30<br>
30 is inserted at first<br>
Linked list contains : 30 20 10<br>
__________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:3<br>
Linked list contains : 30 20 10<br>
__________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:2<br>
30 deleted from first<br>
Linked list contains : 20 10<br>
__________<br>
Operations on singly linked list<br>
__________<br>
1.Inset at first<br>
2.Delete at first<br>
3.Display<br>
4.Exit<br>
Enter your choice:4<br>

--------------------------------<br>
   https://www.iare.ac.in/sites/default/files/DAA%20%20Notes%20by%20Dr.%20L.%20V.%20Narasimha%20Prasad_0.pdf<br>
1.	Write a C++ program to implement singly linked list.
2.	Write a C++ program to split the linked list into two halves such that the element ‘e’ should be the first element of second list.
3.	Find the subset of a given set S = {S1,S2,S3,………,Sn} OF ‘n’ positive integers whose sum is equal to a given positive integer d.
4.	Write a C++ program to implement binary tree and binary search tree.
5.	Write a program to create a WAP to store a k keys into an array of size n at the location compute using a hash function, loc=key%n, where k<=n and key takes 	      values from [1 to m], m>n. Handle the collision using Linear Probing technique.
6.	Write a C++ program to implement doubly linked list.
7.	Write a program to insertion into an AVL tree and deletion from an AVL tree.
8.	Finding minimum and maximum from given unsorted array by using divide conquer method.
9.	Crete a program to merge sort using divide and conquer array.
10.	Write a C++ program for solving the N-Queen’s Problem using backtracking.
11.	Write a program to implement breadth first search for undirected graph (BFS).
12.	Write a program to implement depth first search for undirected graph (DFS).
<br>
<br>
<br>
AI:-
1.Write a python program to find square root
number = int(input("enter a number: "))
sqrt = number ** 0.5
print("square root:", sqrt)
Output:-
enter a number: 100
square root: 10.0
2.Python program to solve quadratic equations
import cmath
x = 1
y = 4
z = 5
w = (y**2) - (4xz)
sol1 = (-y-cmath.sqrt(w))/(2x)
sol2 = (-y+cmath.sqrt(w))/(2x)
print('The solution are {0} and {1}'.format(sol1,sol2))
Output:-
The solution are (-2-1j) and (-2+1j)
3.Program to swap two variables using python
x = 5
y = 16
temp = x
x = y
y = temp
print('The value of x after swapping: {}'.format(x))
print('The value of y after swapping: {}'.format(y))
Output:-
The value of x after swapping: 16
The value of y after swapping: 5
4.python program to check armstrong number
num = int(input("Enter a number: "))
sum = 0
temp = num
while temp > 0
: digit = temp % 10
sum += digit ** 3
temp //= 10
if num == sum:
print(num,"is an Armstrong number")
else:
print(num,"is not an Armstrong number")
Output:-
Enter a number: 2
2 is not an Armstrong number
Enter a number: 1
1 is an Armstrong number
5.find GCD and HCF
def compute_hcf(x, y):
if x > y:
smaller = y else:
smaller = x
for i in range(1, smaller+1):
if((x % i == 0) and (y % i == 0)):
hcf = i
return hcf
num1 = 54
num2 = 24
print("The H.C.F. is", compute_hcf(num1, num2))
Output:-
The H.C.F. is 6
6.find LCM
def compute_lcm(x, y):
if x > y:
greater = x
else:
greater = y

while(True):<br>
   if((greater % x == 0) and (greater % y == 0)):<br>
       lcm = greater<br>
       break<br>
   greater += 1<br>
return lcm<br>
num1 = 54
num2 = 24
print("The L.C.M. is", compute_lcm(num1, num2))
Output:-
The L.C.M. is 216
7.add two two matrix
X = [[12,7,3],
[4 ,5,6],
[7 ,8,9]]

Y = [[5,8,1],
[6,7,3],
[4,5,9]]

result = [[0,0,0],
[0,0,0],
[0,0,0]]
for i in range(len(X)):
for j in range(len(X[0])):
result[i][j] = X[i][j] + Y[i][j]

for r in result:
print(r)
output:- [17, 15, 4]
[10, 12, 9]
[11, 13, 18]


8.covert a string data and time
from datetime import datetime

my_date_string = "Mar 11 2011 11:31AM"

datetime_object = datetime.strptime(my_date_string, '%b %d %Y %I:%M%p')

print(type(datetime_object))
print(datetime_object)
Output:-
<class 'datetime.datetime'>
2011-03-11 11:31:00

9.apend a file
file1 = open("myfile.txt", "w")
L = ["This is Delhi \n", "This is Paris \n", "This is London"]
file1.writelines(L)
file1.close()

Append-adds at last
file1 = open("myfile.txt", "a") # append mode
file1.write("Today \n")
file1.close()

file1 = open("myfile.txt", "r")
print("Output of Readlines after appending")
print(file1.read())
print()
file1.close()

Write-Overwrites
file1 = open("myfile.txt", "w") # write mode
file1.write("Tomorrow \n")
file1.close()

file1 = open("myfile.txt", "r")
print("Output of Readlines after writing")
print(file1.read())
print()
file1.close()
Output:-
Output of Readlines after appending
This is Delhi
This is Paris
This is LondonToday

Output of Readlines after writing
Tomorrow
10.reverse a number
num = 1234
reversed_num = 0

while num != 0:
digit = num % 10
reversed_num = reversed_num * 10 + digit
num //= 10

print("Reversed Number: " + str(reversed_num))
output:-*
Reversed Number: 4321
11.program to compute a power of a number.

<br>
<br>

