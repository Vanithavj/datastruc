1.**C++ program to search a element using binary search**

#include<iostream><br>
using namespace std;<br>
int binarySearch(int arr[], int p, int r, int num) <br>{<br>
   if (p <= r) <br>{<br>
      int mid = (p + r)/2;<br>
      if (arr[mid] == num)<br>
         return mid ;<br>
      if (arr[mid] > num)<br>
         return binarySearch(arr, p, mid-1, num);<br>
      if (arr[mid] < num)<br>
         return binarySearch(arr, mid+1, r, num);<br>
   }<br>
   return -1;<br>
}<br>
int main(void)<br>
 {<br>
   int arr[] = {1, 3, 7, 15, 18, 20, 25, 33, 36, 40};<br>
   int n = sizeof(arr)/ sizeof(arr[0]);<br>
   int num;<br>
   cout << "Enter the number to search: \n";<br>
   cin >> num;<br>
   int index = binarySearch (arr, 0, n-1, num);<br>
   if(index == -1)<br>{<br>
      cout<< num <<" is not present in the array";<br>
   }<br>else<br>{<br>
      cout<< num <<" is present at index "<< index <<" in the array";<br>
   }<br>
   return 0;<br>
}<br>
  
  ![image](https://user-images.githubusercontent.com/97940332/154891861-b9e5a4d9-62be-4861-8e65-2f43fd7c4992.png)
![image](https://user-images.githubusercontent.com/97940332/154892327-b30d97c9-a590-47ec-be74-120bb284d01a.png)

  
  
   ** 2.//Write a C++ program to implement Singly Linked List**
   #include<iostream><br>
#include<cstdlib><br>
using namespace std;<br>
struct node<br>
{<br>
	int info;struct node *next;<br>
}*start;<br>
class single_LL<br>
{<br>
	public:<br>
		node* create_node(int);<br>
		void insert_begin();<br>
		void insert_last();<br>
		void insert_pos();<br>
		void delete_begin();<br>
		void delete_last();<br>
		void delete_pos();<br>
		void update_begin();<br>
		void update_last();<br>
		void update_pos();<br>
		void sort();<br>
		void reverse();<br>
		void search();<br>
		void display();<br>
		single_LL()<br>
		{<br>
			start=NULL;<br>
		}<br>
	};<br>
	int main()<br>
	{<br>
	int choice;<br>
	single_LL sl,s2;<br>
 	start = NULL;<br>
 	do<br>
 	{<br>
 		cout<<"-------------------------"<<endl;<br>
 		cout<<"Operations on singly linked list"<<endl;<br>
 		cout<<"-------------------------"<<endl;<br>
 		cout<<"1.Insertion at first"<<endl;<br>
 		cout<<"2.Insertion at last"<<endl;<br>
 		cout<<"3.Insertion at position"<<endl;<br>
 		cout<<"4.Delete at first"<<endl;<br>
 		cout<<"5.Delete at last"<<endl;<br>
 		cout<<"6.Delete at position"<<endl;<br>
 		cout<<"7.Update at first"<<endl;<br>
 		cout<<"8.Update at last"<<endl;<br>
 		cout<<"9.Update at position"<<endl;<br>
 		cout<<"10.Ascending order"<<endl;<br>
 		cout<<"11.Descending order"<<endl;<br>
 		cout<<"12.Search"<<endl;<br>
 		cout<<"13.Display"<<endl;<br>
 		cout<<"14.Exit"<<endl;<br>
 		cout<<"Enter your choice:";<br>
 		cin>>choice;<br>
 		switch(choice)<br>
 		{<br>
 			
 case 1:<br> sl.insert_begin();<br> 
 sl.display(); <br>
 break;<br> 
 case 2: <br>sl.insert_last();<br> 
 sl.display();<br> 
 break; <br>
 case 3: sl.insert_pos();<br> 
 sl.display(); <br>
 break; <br>
 case 4: s2.delete_begin(); <br>
 sl.display(); <br>
 break; <br>
 case 5: s2.delete_last(); <br>
 sl.display(); <br>
 break; <br>
 case 6: sl.delete_pos(); 
 sl.display(); 
 break; 
 case 7: sl.update_begin(); 
 sl.display(); 
 break; 
 case 8: sl.update_last(); 
 sl.display(); 
 break; 
 case 9: sl.update_pos(); 
 sl.display(); 
 break; 
 case 10:sl.sort(); 
 sl.display(); 
 break; 
 case 11:sl.reverse(); 
 sl.display(); 
 break; 
 case 12:sl.search(); 
 sl.display(); 
 break; 
 case 13:sl.display(); 
 break; 
 case 14:exit(0); 
 break; 
 default:cout<<"Wrong choice...???"<<endl; 
 break; 
 } 
 } 
 while(choice != 14); 
} 
node *single_LL::create_node(int value) 
{ 
 struct node *temp, *s; 
 temp = new(struct node); 
 if (temp == NULL) 
 { 
 cout<<"Memory not allocated"<<endl; 
 return 0; 
 } 
 else 
 { 
 temp->info = value; 
 temp->next = NULL; 
 return temp; 
 } 
} 
void single_LL::insert_begin() 
{ 
 int value; 
 cout<<"Enter the value to be inserted : "; 
 cin>>value; 
 struct node *temp, *s; 
 temp = create_node(value); 
 if (start == NULL) 
 { 
 start = temp; 
 start->next = NULL; 
 cout<<temp->info<<" is inserted at first in the empty list"<<endl; 
 } 
 else 
 { 
 s = start; 
 start = temp; 
 start->next = s; 
 cout<<temp->info<<" is inserted at first"<<endl; 
 } 
} 
void single_LL::insert_last() 
{ 
 int value; 
 cout<<"Enter the value to be inserted : "; 
 cin>>value; 
 struct node *temp, *s; 
 temp = create_node(value); 
 if (start == NULL) 
 { 
 start = temp; 
 start->next = NULL; 
 cout<<temp->info<<" is inserted at last in the empty list"<<endl; 
 } 
 else 
 { 
 s = start; 
 while (s->next != NULL) 
 { 
 s = s->next; 
 } 
 temp->next = NULL; 
 s->next = temp; 
 cout<<temp->info<<" is inserted at last"<<endl; 
 } 
} 
void single_LL::insert_pos() 
{ 
 int value, pos, counter = 0, loc = 1; 
 struct node *temp, *s, *ptr; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 if (counter == 0){} 
 else 
 { 
 cout<<"Enter the postion from "<<loc<<" to "<<counter+1<<" : "; 
 cin>>pos; 
 s = start; 
 if(pos == 1) 
 { 
 cout<<"Enter the value to be inserted : "; 
 cin>>value; 
 temp = create_node(value); 
 start = temp; 
 start->next = s; 
 cout<<temp->info<<" is inserted at first"<<endl; 
 } 
 else if (pos > 1 && pos <= counter) 
 { 
 cout<<"Enter the value to be inserted : "; 
 cin>>value; 
 temp = create_node(value); 
 for (int i = 1; i < pos; i++) 
 { 
 ptr = s; 
 s = s->next; 
 } 
 ptr->next = temp; 
 temp->next = s; 
 cout<<temp->info<<" is inserted at position "<<pos<<endl; 
 } 
 else if (pos == counter+1) 
 { 
 cout<<"Enter the value to be inserted : "; 
 cin>>value; 
 temp = create_node(value); 
 while (s->next != NULL) 
 { 
 s = s->next; 
 } 
 temp->next = NULL; 
 s->next = temp; 
 cout<<temp->info<<" is inserted at last"<<endl; 
 } 
 else 
 { 
 cout<<"Positon out of range...!!!"<<endl; 
 } 
 } 
} 
void single_LL::delete_begin() 
{ 
 if (start == NULL){} 
 else 
 { 
 struct node *s, *ptr; 
 s = start; 
 start = s->next; 
 cout<<s->info<<" deleted from first"<<endl; 
 free(s); 
 } 
} 
void single_LL::delete_last() 
{ 
 int i, counter = 0; 
 struct node *s, *ptr; 
 if (start == NULL){} 
 else 
 { 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 s = start; 
 if (counter == 1) 
 { 
 start = s->next; 
 cout<<s->info<<" deleted from last"<<endl; 
 free(s); 
 } 
 else 
 { 
 for (i = 1;i < counter;i++) 
 { 
 ptr = s; 
 s = s->next; 
 } 
 ptr->next = s->next; 
 cout<<s->info<<" deleted from last"<<endl; 
 free(s); 
 } 
 } 
} 
void single_LL::delete_pos() 
{ 
 int pos, i, counter = 0, loc = 1; 
 struct node *s, *ptr; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 if (counter == 0){} 
 else 
 { 
 if (counter == 1) 
 { 
 cout<<"Enter the postion [ SAY "<<loc<<" ] : "; 
 cin>>pos; 
 s = start; 
 if (pos == 1) 
 { 
 start = s->next; 
 cout<<s->info<<" deleted from first"<<endl; 
 free(s); 
 } 
 else 
 cout<<"Position out of range...!!!"<<endl; 
 } 
 else 
 { 
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : "; 
 cin>>pos; 
 s = start; 
 if (pos == 1) 
 { 
 start = s->next; 
 cout<<s->info<<" deleted from first"<<endl; 
 free(s); 
 } 
 else if (pos > 1 && pos <= counter) 
 { 
 for (i = 1;i < pos;i++) 
 { 
 ptr = s; 
 s = s->next; 
 } 
 ptr->next = s->next; 
 if(pos == counter) 
 {cout<<s->info<<" deleted from last"<<endl; 
 free(s);} 
 else 
 {cout<<s->info<<" deleted from postion "<<pos<<endl; 
 free(s);} 
 } 
 else 
 cout<<"Position out of range...!!!"<<endl; 
 } 
 } 
} 
void single_LL::update_begin() 
{ 
 int value, pos=1, i,counter = 0; 
 struct node *s, *ptr; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 if (counter == 0){} 
 else if (pos == 1) 
 { 
 cout<<"Enter the new node : "; 
 cin>>value; 
 start->info = value; 
 cout<<"Node updated at first position : "<<pos<<" = "<<start->info<<endl; 
 } 
} 
void single_LL::update_last() 
{ 
 int value, pos, i,counter = 0; 
 struct node *s, *ptr; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 s=start; 
 if (counter == 0){} 
 else 
 { 
 cout<<"Enter the new node : "; 
 cin>>value; 
 for (i = 1; i < counter ; i++) 
 { 
 s = s->next; 
 } 
 s->info = value; 
 cout<<"Node updated at last position : "<<counter<<" = "<<s->info<<endl; 
 } 
} 
void single_LL::update_pos() 
{ 
 int value, pos, i,counter = 0, loc = 1; 
 struct node *s, *ptr; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 if (counter == 0){} 
 else 
 { 
 if (counter == 1) 
 { 
 cout<<"Enter the postion [ SAY "<<loc<<" ] : "; 
 cin>>pos; 
 s = start; 
 if (pos == 1) 
 { 
 cout<<"Enter the new node : "; 
 cin>>value; 
 start->info = value; 
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl; 
 } 
 else 
 cout<<"Position out of range...!!!"<<endl; 
 } 
 else 
 { 
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : "; 
 cin>>pos; 
 s = start; 
 if (pos == 1) 
 { 
 cout<<"Enter the new node : "; 
 cin>>value; 
 start->info = value; 
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl; 
 } 
 else if (pos > 1 && pos <= counter) 
 { 
 cout<<"Enter the new node : "; 
 cin>>value; 
 for (i = 1; i < pos ; i++) 
 { 
 s = s->next; 
 } 
 s->info = value; 
 cout<<"Node updated at position : "<<pos<<" = "<<s->info<<endl; 
 } 
 else 
 cout<<"Position out of range...!!!"<<endl; 
 } 
 } 
} 
void single_LL::sort() 
{ 
 struct node *ptr, *s; 
 int value; 
 if (start == NULL){} 
 else 
 { 
 ptr = start; 
 while (ptr != NULL) 
 { 
 for (s = ptr->next;s !=NULL;s = s->next) 
 { 
 if (ptr->info > s->info) 
 { 
 value = ptr->info; 
 ptr->info = s->info; 
 s->info = value; 
 } 
 } 
 ptr = ptr->next; 
 } 
 } 
} 
void single_LL::reverse() 
{ 
 struct node *ptr, *s; 
 int value; 
 if (start == NULL){} 
 else 
 { 
 ptr = start; 
 while (ptr != NULL) 
 { 
 for (s = ptr->next;s !=NULL;s = s->next) 
 { 
 if (ptr->info < s->info) 
 { 
 value = ptr->info; 
 ptr->info = s->info; 
 s->info = value; 
 } 
 } 
 ptr = ptr->next; 
 } 
 } 
} 
void single_LL::search() 
{ 
 int value, loc = 0, pos = 0, counter = 0; 
 struct node *s; 
 s = start; 
 while (s != NULL) 
 { 
 s = s->next; 
 counter++; 
 } 
 if (start == NULL){} 
 else 
 { 
 cout<<"Enter the value to be searched : "; 
 cin>>value; 
 struct node *s; 
 s = start; 
 while (s != NULL) 
 { 
 pos++; 
 if (s->info == value) 
 { 
 loc++; 
 if(loc == 1) 
 cout<<"Element "<<value<<" is found at position "<<pos; 
 else if(loc <= counter) 
 cout<<" , "<<pos; 
 } 
 s = s->next; 
 } 
 cout<<endl; 
 if (loc == 0) 
 cout<<"Element "<<value<<" not found in the list"<<endl; 
 } 
} 
void single_LL::display() 
{ 
 struct node *temp; 
 if (start == NULL) 
 cout<<"Linked list is empty...!!!"<<endl; 
 else 
 { 
 cout<<"Linked list contains : "; 
 temp = start; 
 while (temp != NULL) 
 { 
 cout<<temp->info<<" "; 
 temp = temp->next; 
 } 
 cout<<endl; 
}
}<br><br>


		 


		


   
   
