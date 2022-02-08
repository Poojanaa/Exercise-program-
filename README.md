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
   
