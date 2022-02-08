**1.C++ program to implement singly linked list**<br>
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
