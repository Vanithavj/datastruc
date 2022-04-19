**example1:Add 10 numbers using different loops and note the time complexity of each**

#include<iostream>

using namespace std;<br>
int main()<br>
{<br>
	int i,a[10],sum=0,num,opt;<br>
	cout<<"Enter the number of elements:";<br>
	cin>>num;<br>
	cout<<"Enter the elements:";<br>
	for(i=0;i<num;i++)<br>
	{<br>
		cin>>a[i];<br>
	}<br>
	cout<<"Select a loop which you want: \n1.For loop \n2.While loop \n3.Do-While loop\n Your choice: "<<endl;<br>
	cin>>opt;<br>
	switch(opt)<br>
	{<br>
		case 1: <br>
		for(i=0;i<num;i++)<br>
		{<br>
		sum=sum+a[i];<br>
		}<br>
		cout<<"\n sum= "<<sum<<endl;<br>
		break;<br>
		case 2:<br>
		i=0;	<br>
		while(i<num)<br>
		{<br>
			sum=sum+a[i];<br>
			i++;<br>
		}<br>
		cout<<"\nSum= "<<sum<<endl;<br>
		break;<br>
		case 3:<br>
		i=0;<br>	
		do <br>
		{<br>
		 sum=sum+a[i];<br>
		 i++;<br>
		}while(i<num);<br>
		cout<<"\n Sum= "<<sum<<endl;<br>
		break;<br>
		default:<br>
		cout<<num<<"is Invalid case ";<br>
		break;<br>
	}<br>
}<br><br><br><br>
	**OUTPUT:**
	![image](https://user-images.githubusercontent.com/97940332/162630041-f6ccd4df-d88b-4b4d-b68b-cefa00cf2a78.png)
![image](https://user-images.githubusercontent.com/97940332/162630089-e22b4527-b8b6-40ae-95c9-28fae84500f9.png)
![image](https://user-images.githubusercontent.com/97940332/162630115-68d26f96-c2ff-456e-a5cd-3968bf1b06e4.png)
![image](https://user-images.githubusercontent.com/97940332/162630133-2c1580bd-ab62-4899-936b-146dfee806b5.png)










**1.//C++ program to search a element using binary search**

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
	**OUTPUT:**
  
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
 case 6: sl.delete_pos(); <br>
 sl.display(); <br>
 break; <br>
 case 7: sl.update_begin(); <br>
 sl.display(); <br>
 break; <br>
 case 8: sl.update_last(); <br>
 sl.display(); <br>
 break; <br>
 case 9: sl.update_pos(); <br>
 sl.display(); <br>
 break; <br>
 case 10:sl.sort(); <br>
 sl.display();<br> 
 break; <br>
 case 11:sl.reverse(); <br>
 sl.display(); <br>
 break; <br>
 case 12:sl.search(); <br>
 sl.display(); <br>
 break; <br>
 case 13:sl.display(); <br>
 break; <br>
 case 14:exit(0); <br>
 break;<br> 
 default:cout<<"Wrong choice...???"<<endl; <br>
 break; <br>
 } <br>
 } <br>
 while(choice != 14); <br>
} <br>
node *single_LL::create_node(int value) <br>
{ <br>
 struct node *temp, *s; <br>
 temp = new(struct node); <br>
 if (temp == NULL)<br> 
 { <br>
 cout<<"Memory not allocated"<<endl; <br>
 return 0; <br>
 } <br>
 else <br>
 { <br>
 temp->info = value; <br>
 temp->next = NULL;<br> 
 return temp; <br>
 } <br>
} <br>
void single_LL::insert_begin()<br> 
{ <br>
 int value; <br>
 cout<<"Enter the value to be inserted : "; <br>
 cin>>value; <br>
 struct node *temp, *s; <br>
 temp = create_node(value); <br>
 if (start == NULL) <br>
 {<br> 
 start = temp; <br>
 start->next = NULL;<br> 
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
void single_LL::insert_last() <br>
{ <br>
 int value;<br> 
 cout<<"Enter the value to be inserted : ";<br> 
 cin>>value; <br>
 struct node *temp, *s; <br>
 temp = create_node(value); <br>
 if (start == NULL) <br>
 { <br>
 start = temp;<br> 
 start->next = NULL;<br> 
 cout<<temp->info<<" is inserted at last in the empty list"<<endl; <br>
 } <br>
 else <br>
 { <br>
 s = start; <br>
 while (s->next != NULL) <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 temp->next = NULL;  <br>
 s->next = temp;  <br>
 cout<<temp->info<<" is inserted at last"<<endl;  <br>
 }  <br>
}  <br>
void single_LL::insert_pos()  <br>
{  <br>
 int value, pos, counter = 0, loc = 1;  <br>
 struct node *temp, *s, *ptr;  <br>
 s = start; <br> 
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){}  <br>
 else  <br>
 {  <br>
 cout<<"Enter the postion from "<<loc<<" to "<<counter+1<<" : ";  <br>
 cin>>pos;  <br>
 s = start;  <br>
 if(pos == 1)  <br>
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 start = temp;  <br>
 start->next = s;  <br>
 cout<<temp->info<<" is inserted at first"<<endl; <br> 
 }  <br>
 else if (pos > 1 && pos <= counter)  <br>
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 for (int i = 1; i < pos; i++)  <br>
 {  <br>
 ptr = s;  <br>
 s = s->next;  <br>
 }  <br>
 ptr->next = temp; <br> 
 temp->next = s; <br> 
 cout<<temp->info<<" is inserted at position "<<pos<<endl;  <br>
 }  <br>
 else if (pos == counter+1) <br> 
 {  <br>
 cout<<"Enter the value to be inserted : ";  <br>
 cin>>value;  <br>
 temp = create_node(value);  <br>
 while (s->next != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 temp->next = NULL;  <br>
 s->next = temp;  <br>
 cout<<temp->info<<" is inserted at last"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 cout<<"Positon out of range...!!!"<<endl; <br> 
 }  <br>
 }  <br>
}  <br>
void single_LL::delete_begin()  <br>
{  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl;  <br>
 free(s);  <br>
 }  <br>
}  <br>
void single_LL::delete_last()  <br>
{  <br>
 int i, counter = 0;  <br>
 struct node *s, *ptr;  <br>
 if (start == NULL){} <br> 
 else  <br>
 {  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next; <br>
 counter++;  <br>
 }  <br>
 s = start;  <br>
 if (counter == 1) <br> 
 {  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from last"<<endl;  <br>
 free(s);  <br>
 }  <br>
 else  <br>
 {  <br>
 for (i = 1;i < counter;i++)  <br>
 {  <br>
 ptr = s;  <br>
 s = s->next; <br> 
 }  <br>
 ptr->next = s->next; <br>  
 cout<<s->info<<" deleted from last"<<endl;  <br>
 free(s);  <br>
 }  <br>
 }  <br>
}  <br>
void single_LL::delete_pos()  <br>
{  <br>
 int pos, i, counter = 0, loc = 1;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){} <br> 
 else  <br>
 { <br> 
 if (counter == 1)  <br>
 {  <br>
 cout<<"Enter the postion [ SAY "<<loc<<" ] : ";  <br>
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1) <br> 
 {  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl;  <br>
 free(s);  <br>
 }  <br>
 else <br> 
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : ";  <br>
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 start = s->next;  <br>
 cout<<s->info<<" deleted from first"<<endl;  <br>
 free(s);  <br>
 }  <br>
 else if (pos > 1 && pos <= counter)  <br>
 {  <br>
 for (i = 1;i < pos;i++)  <br>
 {  <br>
 ptr = s; <br> 
 s = s->next;  <br>
 }  <br>
 ptr->next = s->next;  <br>
 if(pos == counter)  <br>
 {cout<<s->info<<" deleted from last"<<endl;  <br>
 free(s);}  <br>
 else  <br>
 {cout<<s->info<<" deleted from postion "<<pos<<endl;  <br>
 free(s);}  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 }  <br> 
}  <br>
void single_LL::update_begin()  <br>
{  <br>
 int value, pos=1, i,counter = 0;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){} <br> 
 else if (pos == 1)  <br>
 {  <br>
 cout<<"Enter the new node : "; <br> 
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at first position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br>
}  <br>
void single_LL::update_last()  <br>
{  <br>
 int value, pos, i,counter = 0;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next; <br> 
 counter++; <br> 
 }  <br>
 s=start;  <br>
 if (counter == 0){}  <br>
 else <br> 
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 for (i = 1; i < counter ; i++)  <br>
 {  <br>
 s = s->next;  <br>
 }  <br>
 s->info = value; <br> 
 cout<<"Node updated at last position : "<<counter<<" = "<<s->info<<endl;  <br>
 }  <br>
}  <br>
void single_LL::update_pos()  <br>
{  <br>
 int value, pos, i,counter = 0, loc = 1;  <br>
 struct node *s, *ptr;  <br>
 s = start;  <br> 
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (counter == 0){}  <br>
 else  <br>
 {  <br>
 if (counter == 1)  <br>
 {  <br>
 cout<<"Enter the postion [ SAY "<<loc<<" ] : "; <br> 
 cin>>pos;  <br>
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 else  <br>
 {  <br>
 cout<<"Enter the postion from "<<loc<<" to "<<counter<<" : ";  <br>
 cin>>pos; <br> 
 s = start;  <br>
 if (pos == 1)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 start->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<start->info<<endl;  <br>
 }  <br> 
 else if (pos > 1 && pos <= counter)  <br>
 {  <br>
 cout<<"Enter the new node : ";  <br>
 cin>>value;  <br>
 for (i = 1; i < pos ; i++)  <br>
 {  <br>
 s = s->next; <br> 
 }  <br>
 s->info = value;  <br>
 cout<<"Node updated at position : "<<pos<<" = "<<s->info<<endl;  <br>
 }  <br>
 else  <br>
 cout<<"Position out of range...!!!"<<endl;  <br>
 }  <br>
 }  <br>
}  <br>
void single_LL::sort()  <br>
{  <br>
 struct node *ptr, *s;  <br>
 int value;  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br> 
 ptr = start;  <br>
 while (ptr != NULL)  <br>
 { <br> 
 for (s = ptr->next;s !=NULL;s = s->next)  <br> <br>
 {  <br>
 if (ptr->info > s->info)  <br>
 { <br> 
 value = ptr->info;  <br> 
 ptr->info = s->info;  <br>
 s->info = value;  <br>
 }  <br>
 }  <br>
 ptr = ptr->next;  <br>
 }  <br>
 }  <br>
}  <br>
void single_LL::reverse()  <br>
{  <br>
 struct node *ptr, *s;  <br>
 int value;  <br>
 if (start == NULL){} <br> 
 else  <br>
 { <br> 
 ptr = start;  <br>
 while (ptr != NULL)  <br>
 {  <br>
 for (s = ptr->next;s !=NULL;s = s->next)  <br>
 {  <br>
 if (ptr->info < s->info)  <br>
 { <br> 
 value = ptr->info;  <br>
 ptr->info = s->info; <br> 
 s->info = value;  <br>
 }  <br>
 }  <br>
 ptr = ptr->next; <br> 
 }  <br>
 }  <br>
}  <br>
void single_LL::search() <br> 
{  <br>
 int value, loc = 0, pos = 0, counter = 0;  <br>
 struct node *s;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 s = s->next;  <br>
 counter++;  <br>
 }  <br>
 if (start == NULL){}  <br>
 else  <br>
 {  <br> 
 cout<<"Enter the value to be searched : ";  <br>
 cin>>value;  <br>
 struct node *s;  <br>
 s = start;  <br>
 while (s != NULL)  <br>
 {  <br>
 pos++;  <br>
 if (s->info == value)  <br>
 {  <br>
 loc++;  <br>
 if(loc == 1)  <br>
 cout<<"Element "<<value<<" is found at position "<<pos;  <br>
 else if(loc <= counter)  <br>
 cout<<" , "<<pos;  <br>
 }  <br>
 s = s->next;  <br>
 }  <br> 
 cout<<endl;  <br>
 if (loc == 0)  <br>
 cout<<"Element "<<value<<" not found in the list"<<endl;  <br>
 }  <br>
} <br> 
void single_LL::display()  <br>
{  <br>
 struct node *temp;  <br>
 if (start == NULL) <br> 
 cout<<"Linked list is empty...!!!"<<endl;  <br>
 else  <br>
 { <br> 
 cout<<"Linked list contains : "; <br> 
 temp = start;  <br>
 while (temp != NULL)  <br>
 {  <br>
 cout<<temp->info<<" "; <br> 
 temp = temp->next;  <br>
 }  <br>
 cout<<endl;  <br>
} <br>
}<br><br>
	

**OUTPUT:**
![image](https://user-images.githubusercontent.com/97940332/154902067-c5f98269-4c2a-4c5e-a48a-a439685e6cad.png)
![image](https://user-images.githubusercontent.com/97940332/154902765-ecf7a91e-9d1f-4e5f-80b4-282a99644072.png)
![image](https://user-images.githubusercontent.com/97940332/154902837-a591fbcf-72a5-4158-a19a-51b9b81a7fb6.png)
![image](https://user-images.githubusercontent.com/97940332/154903004-07e1d2a1-8b9c-425a-a0ae-149c98a89413.png)
![image](https://user-images.githubusercontent.com/97940332/154903073-5a873aa1-a9b7-4236-981c-091f53034d33.png)
![image](https://user-images.githubusercontent.com/97940332/154903172-4cbba4af-e190-49c6-8176-05598245de89.png)
![image](https://user-images.githubusercontent.com/97940332/154903218-450cbc29-4397-4b47-a037-8b6da86536a0.png)
![image](https://user-images.githubusercontent.com/97940332/154903501-0eb24dca-747a-4549-ba42-bf98bfb66a7c.png)
![image](https://user-images.githubusercontent.com/97940332/154903564-80c758c3-85b3-4e9f-95e1-a397ca4fd4d0.png)
![image](https://user-images.githubusercontent.com/97940332/154903743-5f6f1123-f6bb-4406-875e-591ebf648d9b.png)
![image](https://user-images.githubusercontent.com/97940332/154903830-d66c176d-70f0-486b-a75e-f72e35ff3005.png)
![image](https://user-images.githubusercontent.com/97940332/154903967-a55635a8-2958-463d-b94d-a83b2e2dab01.png)
![image](https://user-images.githubusercontent.com/97940332/154904040-ee819643-70d6-4262-9ab1-17c539236d0e.png)

	
**3.//C++ program to implement addition of 2 Arrays.**
	
	
#include<iostream> <br> 
using namespace std; <br>
int main() <br>
{ <br>
	int size, i, arr1[10], arr2[10], add[10]; <br>
	cout << "\nPlease Enter the Array Size =  "; <br>
	cin >> size; <br>
	cout << "\nPlease Enter the First Array elements : "; <br>
	for(i = 0; i < size; i++) <br>
	{ <br>
		cin >> arr1[i]; <br>
	} <br>	
	cout << "\nPlease Enter the Second Array elements :  "; <br>
	for(i = 0; i < size; i++) <br>
	{ <br>
		cin >> arr2[i]; <br>
	} <br>
	for(i = 0; i < size; i++) <br>
	{ <br>
		add[i] = arr1[i] + arr2[i]; <br>
		cout << arr1[i] << " + " << arr2[i] << " = " << add[i] << "\n"; <br>
	} <br>
	cout << "\nThe Final Result of adding 2 One Dimensional Arrays = "; <br>
	for(i = 0; i < size; i++) <br>
	{ <br>
		cout << add[i] << " "; <br>
	} <br>
return 0; <br>
 } <br> <br>
	
	
	
**OUTPUT:**
	
	![image](https://user-images.githubusercontent.com/97940332/154905267-fdcfe64d-7ebf-4068-b88d-4c1149373b05.png)
	
	
	
**4.//C++ Program to implement reverse order of array elements**
	
	
#include <iostream>  <br>
using namespace std;<br>  
int main ()  <br>
{  <br>
    int arr[50], num, temp, i, j; <br> 
    cout << " Please, enter the total no. you want to enter: ";  <br>
    cin >> num;  <br>
    cout << " Enter the element : ";  <br>
    for (i = 0; i < num; i++)  <br>
    {  <br>
        cin >> arr[i];<br>  
    }  <br>
     for ( i = 0, j = num - 1; i < num/2; i++, j--)  <br>
    {   <br>  
        temp = arr[i];  <br>
        arr[i] = arr[j];  <br>
        arr[j] = temp;  <br>
    }  <br>
    cout << "\n Reverse order of an array: " << endl; <br> 
    for ( i = 0; i < num; i++) <br> 
    {  <br>
        cout << arr[i] << " "; <br> 
    }  <br>
    return 0;<br>  
}  <br>
	**OUTPUT:**
	
	
	![image](https://user-images.githubusercontent.com/97940332/154906061-70cfb7f0-3086-4b25-83fb-27ea3991ea4e.png)


**5.//Program to implementing stack using array.**
	
	
	
#include<stdio.h><br>
int stack[100],choice,n,top,x,i;<br>
void push(void);<br>
void pop(void);<br>
void display(void);<br>
int main()<br>
{<br>
    //clrscr();<br>
    top=-1;<br>
    printf("\n Enter the size of STACK[MAX=100]:");<br>
    scanf("%d",&n);<br>
    printf("\n\t STACK OPERATIONS USING ARRAY");<br>
    printf("\n\t--------------------------------");<br>
    printf("\n\t 1.PUSH\n\t 2.POP\n\t 3.DISPLAY\n\t 4.EXIT");<br>
    do<br>
    {<br>
        printf("\n Enter the Choice:");<br>
        scanf("%d",&choice);<br>
        switch(choice)<br>
        {<br>
            case 1:<br>
            {<br>
                push();<br>
                break;<br>
            }<br>
            case 2:<br>
            {<br>
                pop();<br>
                break;<br>
            }<br>
            case 3:<br>
            {<br>
                display();<br>
                break;<br>
            }<br>
            case 4:<br>
            {<br>
                printf("\n\t EXIT POINT ");<br>
                break;<br>
            }<br>
            default:<br>
            {<br>
                printf ("\n\t Please Enter a Valid Choice(1/2/3/4)");<br>
            }<br>
           }<br>
	}<br>
    while(choice!=4);<br>
    return 0;<br>
}<br>
void push()<br>
{<br>
    if(top>=n-1)<br>
    {<br>
        printf("\n\tSTACK is over flow");<br>
     }<br>
    else<br>
    {<br>
        printf(" Enter a value to be pushed:");<br>
        scanf("%d",&x);<br>
        top++;<br>
        stack[top]=x;<br>
    }<br>
}<br>
void pop()<br>
{<br>
    if(top<=-1)<br>
    {<br>
        printf("\n\t Stack is under flow");<br>
    }<br>
    else<br>
    {<br>
        printf("\n\t The popped elements is %d",stack[top]);<br>
        top--;<br>
    }<br>
}<br>
void display()<br>
{<br>
    if(top>=0)<br>
    {<br>
        printf("\n The elements in STACK \n");<br>
        for(i=top; i>=0; i--)<br>
            printf("\n%d",stack[i]);<br>
        printf("\n Press Next Choice");<br>
    }<br>
    else<br>
    {<br>
        printf("\n The STACK is empty");<br>
    }<br>
}<br>
	
**OUTPUT:**
	
	
![image](https://user-images.githubusercontent.com/97940332/154907349-69233a1a-9bc2-46d8-a3a4-83aafb8358e3.png)
	
	
	
	
	
	
	
	
	
	
	
	
	
	

	
	
**6.//Write a C++ program to split the given linked list into 2 in such a way that the given element ele must be the first node of second linked list	**
	
	
	
#include<iostream><br>
using namespace std;<br>
struct Node<br>
{<br>
	int value;<br>
	struct Node *next;<br>
};<br>
struct Node*head=NULL;<br>
struct  Node*sHead=NULL;<br>
struct Node*temp=NULL;<br>
void insert(int new_data)<br>
{<br>
struct Node *new_node=new Node();<br>
	new_node->value=new_data;<br>
	new_node->next=head;<br>
	head=new_node;<br>
}<br>
int n;<br>
int ele;<br>
int splitIndex;<br>
int main()<br>
{<br>
	int i;<br>
	cout<<"Enter number of elements you want in the list:\t";<br>
	cin>>n;<br>
	cout<<"Enter elements:"<<endl;<br>
	for(i=0;i<n;i++)<br>
	{<br>
		cin>>ele;<br>
		insert(ele);<br>
	}<br>
	cout<<"\nList of elements:"<<endl;<br>
	Node *t;<br>
	t=head;<br>
	while(t!=NULL)<br>
	{<br>
		cout<<t->value<<"\t";<br>
		t=t->next;<br>
	}<br>
	cout<<"\n\nEnter the position you want the list to split:";<br>
	cin>>splitIndex;<br>
	while(splitIndex<0||splitIndex>n-1)<br>
	{<br>
		cout<<"Invalid position.Try again"<<endl;<br>
		cin>>splitIndex;<br>
	}<br>
	temp=head;<br>
	for(i=0;i<=splitIndex;i++)<br>
	{<br>
		if(i==splitIndex-1)<br>
		{<br>
			Node *tN;<br>
			tN=temp->next;<br>
			sHead=tN;<br>
			temp->next=NULL;<br>
			break;<br>
		}<br>
		temp=temp->next;<br>
	}<br>
	temp=head;<br>
	if(temp==NULL)<br>
	{<br>
		cout<<"\nFirst list is empty"<<endl;<br>
	}else<br>
	{<br>
	cout<<"\n\nFirst list element is:"<<endl;<br>
	while(temp!=NULL)<br>
	{<br>
	cout<<temp->value<<"\t";<br>
	temp=temp->next;<br>
	}<br>	
	}<br>
	temp=sHead;<br>
	if(temp==NULL)<br>
	{<br>
		cout<<"\nSecond list is empty"<<endl;<br>
	}<br>
	else<br>
	{<br>
		cout<<"\n\nSecond list elements is:"<<endl;<br>
		while(temp!=NULL)<br>
		{<br>
			cout<<temp->value<<"\t";<br>
			temp=temp->next;<br>
		}<br>
	}<br>
	return 0;<br>
}<br><br><br>
	
**OUTPUT:**
	
	
	
	![image](https://user-images.githubusercontent.com/97940332/154908510-d520df33-0f3c-4995-9e8f-3f10966a834b.png)
	![image](https://user-images.githubusercontent.com/97940332/154908687-b6619d22-e708-47c6-856d-11a82369c3ca.png)

	
	
	
	
**7.Construct a binary searchtree (BST) to support the following operations.
	Given a key,perform a search in the BST.If the key is found then display "key found".
	i.Insert an element into a binary search tree.
	ii.Delete an element from a binary serch tree.
	Display the tree using inorder,preorder and postorder traversal method.**
	

	
	
	
#include <iostream><br> 
#include <cstdlib> <br>
using namespace std; <br>
struct node <br>
{ <br>
 int info;<br> 
 struct node *left; <br>
 struct node *right; <br>
}*root; <br>
class BST <br>
{ <br>
 public:<br> 
 void find(int, node **, node **); <br>
 void insert(node *, node *); <br>
 void del(int); <br>
 void case_a(node *,node *); <br>
 void case_b(node *,node *); <br>
 void case_c(node *,node *); <br>
 void preorder(node *); <br>
 void inorder(node *); <br>
 void postorder(node *); <br>
 void display(node *, int);<br> 
 BST() <br>
{<br>
	root=NULL;<br>
}<br>
};<br>
int main()<br>
{<br>
	int choice,num;<br>
	BST bst;<br>
	node *temp;<br>
	while(1)<br>
	{<br>
		cout<<"------------------"<<endl;<br>
		cout<<"Operations on BST"<<endl;<br>
		cout<<"------------------"<<endl;<br>
		cout<<"1.Insert element"<<endl;<br>
		cout<<"2.Delete element"<<endl;<br>
		cout<<"3.Inorder traversal"<<endl;<br>
		cout<<"4.Preorder traversal"<<endl;<br>
		cout<<"5.Postorder traversal"<<endl;<br>
		cout<<"6.Display"<<endl;<br>
		cout<<"7.Quit"<<endl;<br>
		cout<<"Enter your choice:";<br>
		 cin>>choice; <br>
 switch(choice) <br>
 { <br>
 case 1: <br>
 temp = new node; <br>
 cout<<"Enter the number to be inserted : "; <br>
 cin>>temp->info; <br>
 bst.insert(root, temp); <br>
 break; <br>
 case 2: <br>
 if (root == NULL) <br>
 { <br>
 cout<<"Tree is empty, nothing to delete"<<endl; <br>
 continue; <br>
 } <br>
 cout<<"Enter the number to be deleted : "; <br>
 cin>>num; <br>
 bst.del(num); <br>
 break; <br>
 case 3:<br> 
 cout<<"Inorder Traversal of BST:"<<endl; <br>
 bst.inorder(root); <br>
 cout<<endl; <br>
 break; <br>
 case 4: <br>
 cout<<"Preorder Traversal of BST:"<<endl; <br>
 bst.preorder(root); <br>
 cout<<endl; <br>
 break; <br>
 case 5:<br> 
 cout<<"Postorder Traversal of BST:"<<endl; <br>
 bst.postorder(root); <br>
 cout<<endl; <br>
 break; <br>
 case 6:<br> 
 cout<<"Display BST:"<<endl; <br>
 bst.display(root,1); <br>
 cout<<endl; <br>
 break; <br>
 case 7: <br>
 exit(1); <br>
 default: <br>
 cout<<"Wrong choice"<<endl; <br>
 } <br>
 } <br>
} <br>
void BST::find(int item, node **par, node **loc) <br>
{ <br>
 node *ptr, *ptrsave; <br>
 if (root == NULL) <br>
 { <br>
 *loc = NULL; <br>
 *par = NULL; <br>
 return; <br>
 } <br>
 if (item == root->info) <br>
 { <br>
 *loc = root; <br>
 *par = NULL;<br> 
 return; <br>
 } <br>
 if (item < root->info) <br>
 ptr = root->left; <br>
 else <br>
 ptr = root->right; <br>
 ptrsave = root; <br>
 while (ptr != NULL) <br>
 { <br>
 if (item == ptr->info) <br>
 { <br>
 *loc = ptr; <br>
 *par = ptrsave; <br>
 return; <br>
 } <br>
 ptrsave = ptr; <br>
 if (item < ptr->info)<br> 
 ptr = ptr->left; <br>
 else <br>
 ptr = ptr->right; <br>
 } <br>
 *loc = NULL; <br>
 *par = ptrsave; <br>
} <br>
void BST::insert(node *tree, node *newnode) <br>
{ <br>
 if (root == NULL) <br>
 { <br>
 root = new node; <br>
 root->info = newnode->info;<br> 
 root->left = NULL; <br>
 root->right = NULL; <br>
 cout<<"Root Node is Added"<<endl; <br>
 return; <br>
 } <br>
 if (tree->info == newnode->info) <br>
 { <br>
 cout<<"Element already in the tree"<<endl; <br>
 return; <br>
 } <br>
 if (tree->info > newnode->info) <br>
 { <br>
 if (tree->left != NULL) <br>
 { <br>
 insert(tree->left, newnode); <br>
 } <br>
 else <br>
 { <br>
 tree->left = newnode; <br>
 (tree->left)->left = NULL; <br>
 (tree->left)->right = NULL; <br>
 cout<<"Node Added To Left"<<endl; <br>
 return;<br> 
 } <br>
 } <br>
 else <br>
 { <br>
 if (tree->right != NULL) <br>
 { <br>
 insert(tree->right, newnode); <br>
 } <br>
 else <br>
 { <br>
 tree->right = newnode; <br>
 (tree->right)->left = NULL;<br> 
 (tree->right)->right = NULL;<br> 
 cout<<"Node Added To Right"<<endl; <br>
 return; <br>
 } <br>
 } <br>
} <br>

void BST::del(int item) <br>
{ <br>
 node *parent, *location; <br>
 if (root == NULL) <br>
 { <br>
 cout<<"Tree empty"<<endl; <br>
 return; <br>
 } <br>
 find(item, &parent, &location); <br>
 if (location == NULL) <br>
 { <br>
 cout<<"Item not present in tree"<<endl; <br>
 return;<br> 
 } <br>
 if (location->left == NULL && location->right == NULL) <br>
 case_a(parent, location); <br>
 if (location->left != NULL && location->right == NULL) <br>
 case_b(parent, location); <br>
 if (location->left == NULL && location->right != NULL) <br>
 case_b(parent, location); <br>
 if (location->left != NULL && location->right != NULL) <br>
 case_c(parent, location); <br>
 free(location); <br>
} <br>
 void BST::case_a(node *par, node *loc ) <br>
{ <br>
 if (par == NULL) <br>
 { <br>
 root = NULL; <br>
 } <br>
 else <br>
 { <br>
 if (loc == par->left) <br>
 par->left = NULL; <br>
 else <br>
 par->right = NULL; <br>
 } <br>
} <br>
 void BST::case_b(node *par, node *loc) <br>
{ <br>
 node *child; <br>
 if (loc->left != NULL) <br>
 child = loc->left; <br>
 else <br>
 child = loc->right; <br>
 if (par == NULL) <br>
 { <br>
 root = child; <br>
 } <br>
 else <br>
 { <br>
 if (loc == par->left) <br>
 par->left = child;<br> 
 else <br>
 par->right = child; <br>
 } <br>
} <br>
 void BST::case_c(node *par, node *loc)<br> 
{ <br>
 node *ptr, *ptrsave, *suc, *parsuc; <br>
 ptrsave = loc; <br>
 ptr = loc->right;<br> 
 while (ptr->left != NULL) <br>
 { <br>
 ptrsave = ptr; <br>
 ptr = ptr->left; <br>
 } <br>
 suc = ptr; <br>
 parsuc = ptrsave; <br>
 if (suc->left == NULL && suc->right == NULL) <br>
 case_a(parsuc, suc); <br>
 else <br>
 case_b(parsuc, suc); <br>
 if (par == NULL) <br>
 { <br>
 root = suc; <br>
 } <br>
 else <br>
 { <br>
 if (loc == par->left)<br> 
 par->left = suc; <br>
 else <br>
 par->right = suc<br>; 
 } <br>
 suc->left = loc->left; <br>
 suc->right = loc->right; <br>
} <br>
 void BST::preorder(node *ptr) <br>
{ <br>
 if (root == NULL) <br>
 { <br>
 cout<<"Tree is empty"<<endl; <br>
 return; <br>
 } <br>
 if (ptr != NULL) <br>
 { <br>
 cout<<ptr->info<<" "; <br>
 preorder(ptr->left); <br>
 preorder(ptr->right); <br>
 } <br>
} <br>
void BST::inorder(node *ptr) <br>
{ <br>
 if (root == NULL) <br>
 { <br>
 cout<<"Tree is empty"<<endl; <br>
 return; <br>
 } 
 if (ptr != NULL) <br>
 { 
 inorder(ptr->left); <br>
 cout<<ptr->info<<" "; <br>
 inorder(ptr->right); <br>
 } <br>
} <br>
 
void BST::postorder(node *ptr) <br>
{ <br>
 if (root == NULL) <br>
 { <br>
 cout<<"Tree is empty"<<endl; <br>
 return; <br>
 } <br>
 if (ptr != NULL) <br>
 { <br>
 postorder(ptr->left); <br>
 postorder(ptr->right); <br>
 cout<<ptr->info<<" "; <br>
 } <br>
} <br>
void BST::display(node *ptr, int level) <br>
{ <br>
 int i; <br>
 if (ptr != NULL) <br>
 { <br>
 display(ptr->right, level+1); <br>
 cout<<endl;<br> 
 if (ptr == root) <br>
 cout<<"Root->: "; <br>
 else<br> 
 { <br>
 for (i = 0;i < level;i++) <br>
 cout<<" "; <br>
 }<br> 
 cout<<ptr->info; <br>
 display(ptr->left, level+1); <br>
 } <br>
}<br>

	**OUTPUT:**
	



![image](https://user-images.githubusercontent.com/97940332/155080654-b9477903-f8f9-4502-bb64-94b385bce01c.png)
![image](https://user-images.githubusercontent.com/97940332/155080747-78e6416d-175f-4a7e-8d5a-b7483d428e1e.png)
![image](https://user-images.githubusercontent.com/97940332/155080815-b4d8a7f0-3a8c-4a7a-a4b1-261274195c72.png)
![image](https://user-images.githubusercontent.com/97940332/155081162-ff981b2d-1ce3-4818-9c19-b4813c271249.png)
![image](https://user-images.githubusercontent.com/97940332/155081454-7306a119-9553-4c6a-a1e5-a28a24062081.png)

	
	
	
**8.// C++ program for implementation min heap Sort**<br>
#include <iostream><br>
using namespace std;<br>
void heapify(int arr[], int n, int i)<br>
{<br>
    int largest = i; <br>
    int l = 2 * i + 1; <br>
    int r = 2 * i + 2; <br>
  if (l < n && arr[l] > arr[largest])<br>
        largest = l;<br>
    if (r < n && arr[r] > arr[largest])<br>
        largest = r;<br>
    if (largest != i)<br> {<br>
        swap(arr[i], arr[largest]);<br>
        heapify(arr, n, largest);<br>
    }<br>
}<br>
void heapSort(int arr[], int n)<br>
{<br>
    for (int i = n / 2 - 1; i >= 0; i--)<br>
        heapify(arr, n, i);<br>
  
    for (int i = n - 1; i >= 0; i--)<br> {<br>
        swap(arr[0], arr[i]);<br>
        heapify(arr, i, 0);<br>
    }<br>
}<br>
void printArray(int arr[], int n)<br>
{<br>
    for (int i = 0; i < n; ++i)<br>
        cout << arr[i] << " ";<br>
    cout << "\n";<br>
}<br>
int main()<br>
{<br>
    int arr[50] ,n;<br>
    cout<<"Enter the number of element to be sorted:";<br>
    cin>>n;<br>
    
    for(int i=0;i<n;i++)<br>
    {<br>
    	cout<<"Enter element "<<i+1<<":";<br>
    	cin>>arr[i];<br>
	}<br>
  heapSort(arr, n);<br>
  
    cout << "Sorted array is \n";<br>
    printArray(arr, n);<br>
}<br>
	
	
	
**OUTPUT:**
	
	
	
	
	
	
	
	
	
	
	
	
![image](https://user-images.githubusercontent.com/97940332/155941254-9e58a578-d4b9-43e7-b594-a82c6ff29c8d.png)
	
	
**9.// C++ program for implementation max heap  Sort**
	
	
#include <bits/stdc++.h><br>
using namespace std;<br>
 void heapify(int arr[], int n, int i)
{<br>
    int smallest = i; <br>
    int l = 2 * i + 1;<br>
    int r = 2 * i + 2;<br> 
    if (l < n && arr[l] < arr[smallest])<br>
        smallest = l;<br>
    if (r < n && arr[r] < arr[smallest])<br>
        smallest = r;
    if (smallest != i) <br>{<br>
        swap(arr[i], arr[smallest]);<br>
        heapify(arr, n, smallest);<br>
    }<br>
}<br>
void heapSort(int arr[], int n)<br>
{
    for (int i = n / 2 - 1; i >= 0; i--)<br>
        heapify(arr, n, i);<br>
 
    for (int i = n - 1; i >= 0; i--) <br>
	{<br>
        swap(arr[0], arr[i]);<br>
        heapify(arr, i, 0);<br>
    }<br>
}<br>
void printArray(int arr[], int n)<br>
{<br>
    for (int i = 0; i < n; ++i)<br>
        cout << arr[i] << " ";<br>
    cout << "\n";<br>
}<br>
int main()<br>
{<br>
    int n,i,arr[50];<br>
    cout<<"Enter the number of elements to be sorted: ";<br>
    cin>>n;<br>
    for(i=0;i<n;i++)<br>
    {<br>
    	cout<<"Enter element "<<i+1<<" :";<br>
    	cin>>arr[i];<br>
	}<br>
 
    heapSort(arr, n);<br>
 
    cout << "Sorted array is \n";<br>
    printArray(arr, n);<br>
}<br>
<br>
	
**OUTPUT:** ![image](https://user-images.githubusercontent.com/97940332/156103830-f50189e4-2c6a-4347-bf6b-b19d67988aea.png)
	
**10.C++ Program to implement maxheap.**
	
#include <iostream><br>
#include <conio.h><br>
using namespace std;<br>
void max_heap(int *a, int m, int n)<br>{<br>
   int j, t;<br>
   t= a[m];<br>
   j = 2 * m;<br>
   while (j <= n)<br> {<br>
      if (j < n && a[j+1] > a[j])<br>
         j = j + 1;<br>
      if (t > a[j])<br>
         break;<br>
      else if (t <= a[j])<br> {<br>
         a[j/2] = a[j];<br>
         j = 2 * j;<br>
      }<br>
   }<br>
   a[j/2] = t;<br>
   return;<br>
}<br>
void build_maxheap(int *a, int n)<br> {<br>
   int k;<br>
   for(k = n/2; k >= 1; k--)<br> {<br>
      max_heap(a,k,n);<br>
   }<br>
}<br>
int main() <br>
{<br>
   int n, i;<br>
   cout<<"Enter number of elements of the array:\n";<br>
   cin>>n;<br>
   int a[30];<br>
   for (i = 1; i <= n; i++)<br> {<br>
      cout<<"Enter element:"<<" "<<(i)<<endl;<br>
      cin>>a[i];<br>
   }<br>
   build_maxheap(a, n);<br>
   cout<<"Max Heap:\n";<br>
   for (i = 1; i <= n; i++) <br>{<br>
      cout<<a[i]<<endl;<br>
   }<br>
   getch();<br>
}<br>
	<br><br><br>
	**OUTPUT:**
	![image](https://user-images.githubusercontent.com/97940332/156984057-d6826aa1-d6d4-4e83-9be6-8828dde2c10b.png)

	
**11.C++ program to implement min heap.**
	
	
#include <iostream><br>
#include <conio.h><br>
using namespace std;<br>
void min_heap(int *a, int m, int n)<br>{<br>
   int j, t;<br>
   t= a[m];<br>
   j = 2 * m;<br>
   while (j <= n)<br> {<br>
      if (j < n && a[j+1] < a[j])<br>
         j = j + 1;<br>
      if (t < a[j])<br>
         break;<br>
      else if (t >= a[j]) <br>{<br>
         a[j/2] = a[j];<br>
         j = 2 * j;<br>
      }<br>
   }<br>
   a[j/2] = t;<br>
   return;<br>
}<br>
void build_minheap(int *a, int n)<br> {<br>
   int k;<br>
   for(k = n/2; k >= 1; k--) <br>{<br>
      min_heap(a,k,n);<br>
   }<br>
}<br>
int main() <br>
{<br>
   int n, i;<br>
   cout<<"Enter number of elements of the array:\n";<br>
   cin>>n;<br>
   int a[30];<br>
   for (i = 1; i <= n; i++)<br> {<br>
      cout<<"Enter element:"<<" "<<(i)<<endl;<br>
      cin>>a[i];<br>
   }<br>
   build_minheap(a, n);<br>
   cout<<"Min Heap:\n";<br>
   for (i = 1; i <= n; i++)<br> {<br>
      cout<<a[i]<<endl;<br>
   }<br>
   getch();<br>
}<br>
	<br><br><br>
	**OUTPUT:**
	![image](https://user-images.githubusercontent.com/97940332/156986498-206941eb-d97c-4d83-af72-679638c1e77e.png)
	
	
	
**12.C++ program to find a subset of given set S={s1,s2,s3........sn} of n positive integer. Whose sum is equal to given positive integer d.**
	
#include <iostream><br>
using namespace std;<br>
class Subset<br>
{<br>
	public:<br>
    void printSum(int result[], int front, int tail)<br>
    {<br>
    	cout << "{";<br>
		for (int i = front; i < tail; ++i)<br>
		{<br>
			if (result[i] != INT_MAX)<br>
			{<br>
				cout << " " << result[i] << " ";<br>
			}<br>
		}<br>
		cout << "}\n";<br>
	}<br>
	void subsetSum(int arr[], int result[], int sum, int size, int current_sum, int location)<br>
	{<br>
		if (location == -1)<br>
		{<br>
			return;<br>
		}<br>
		this->subsetSum(arr, result, sum, size, current_sum, location - 1);<br>
		result[location] = arr[location];<br>
		if (current_sum + arr[location] == sum)<br>
		{<br>
			this->printSum(result, location, size);<br>
		}<br>
		this->subsetSum(arr, result, sum, size, current_sum + arr[location], location - 1);<br>
		result[location] = INT_MAX;<br>
	}<br>
	void findSubset(int arr[], int size, int sum)<br>
	{<br>
		if (size <= 0)<br>
		{<br>
			return;<br>
		}<br>
		int result[size];<br>
		for (int i = 0; i < size; ++i)	<br>	
		{<br>
			result[i] = INT_MAX;<br>
		}<br>
		
		this->subsetSum(arr, result, sum, size, 0, size - 1);<br>
	}<br>
};<br>
int main()<br>
{<br>
	Subset task = Subset();<br>
	int n;<br>
	cout<<"Enter the size of the array:";<br>
	cin>>n;<br>
	int arr[n]={};<br>
	cout<<"Enter the array element:\n";<br>
	for(int i=0;i<n;i++)<br>
	{<br>
		cin>>arr[i];<br>
	}<br>
	int size = sizeof(arr) / sizeof(arr[0]);<br>
int sum;<br>
cout<<"Enter the sum element: ";<br>
cin>>sum;<br>
task.findSubset(arr, size, sum);<br>
return 0;<br>
}<br>
<br><br><br>
	
	
**OUTPUT:**
	
![image](https://user-images.githubusercontent.com/97940332/159217106-e368aae9-868b-48a3-b644-5659754e5c50.png)	
	
![image](https://user-images.githubusercontent.com/97940332/159217650-482be0e8-34e8-4baf-83dc-03c3f46ff1f9.png)


**mergesort**
	
#include <iostream>
#include<conio.h>
using namespace std;<br>
void Merge(int *a, int low, int high, int mid)<br>
{<br>
	int i, j, k, temp[high-low+1];<br>
	i = low;<br>
	k = 0;<br>
        j = mid + 1;<br>
        while (i <= mid && j <= high)<br>
	{<br>
		if (a[i] < a[j])<br>
		{<br>
		temp[k] = a[i];<br>
		k++;<br>
		i++;<br>
		}<br>
		else<br>
		{<br>
		temp[k] = a[j];<br>
		k++;<br>
		j++;<br>
		}<br>
	}<br>
	while (i <= mid)<br>
	{<br>
	temp[k] = a[i];<br>
	k++;<br>
	i++;<br>
	}<br>
	while (j <= high)<br>
	{<br>
	temp[k] = a[j];<br>
	k++;<br>
	j++;<br>
	}<br>
	for (i = low; i <= high; i++)<br>
	{<br>
	a[i] = temp[i-low];<br>
	}<br>
}<br>
void MergeSort(int *a, int low, int high)<br>
{<br>
	int mid;<br>
	if (low < high)<br>
	{<br>
	 mid=(low+high)/2;<br>
	 MergeSort(a, low, mid);<br>
         MergeSort(a, mid+1, high);<br>
	 Merge(a, low, high, mid);<br>
	}<br>
}<br>
int main()<br>
{<br>
	int n, i;<br>
	cout<<"\nEnter the number of data element to be sorted: ";<br>
	cin>>n;<br>
	int arr[n];<br>
	for(i = 0; i < n; i++)<br>
	{<br>
	   cout<<"Enter element "<<i+1<<": ";<br>
	   cin>>arr[i];<br>
	}<br>
         MergeSort(arr, 0, n-1);<br>
	 cout<<"\nSorted Data ";<br>
	 for (i = 0; i < n; i++)<br>
            cout<<"->"<<arr[i];<br>
	 getch();<br>
}<br><br><br><br>
	
**OUTPUT:**
	
	![image](https://user-images.githubusercontent.com/97940332/162896381-23ae9507-9109-498e-a149-401c9bb8cba2.png)

	
	
**Write a program to implement a red black tree**
	
	
#include<iostream>
using namespace std;<br>
struct node<br>
{<br>
       int key;<br>
       node *parent;<br>
       char color;<br>
       node *left;<br>
       node *right;<br>
};<br>
class RBtree<br>
{<br>
      node *root;<br>
      node *q;<br>
   public :<br>
      RBtree()<br>
      {<br>
              q=NULL;<br>
              root=NULL;<br>
      }<br>
      void insert();<br>
      void insertfix(node *);<br>
      void leftrotate(node *);<br>
      void rightrotate(node *);<br>
      void del();<br>
      node* successor(node *);<br>
      void delfix(node *);<br>
      void disp();<br>
      void display( node *);<br>
      void search();<br>
};<br>
void RBtree::insert()<br>
{<br>
     int z,i=0;<br>
     cout<<"\nEnter key of the node to be inserted: ";<br>
     cin>>z;<br>
     node *p,*q;<br>
     node *t=new node;<br>
     t->key=z;<br>
     t->left=NULL;<br>
     t->right=NULL;<br>
     t->color='r';<br>
     p=root;<br>
     q=NULL;<br>
     if(root==NULL)<br>
     {<br>
           root=t;<br>
           t->parent=NULL;<br>
     }<br>
     else<br>
     {<br>
         while(p!=NULL)<br>
         {<br>
              q=p;<br>
              if(p->key<t->key)<br>
                  p=p->right;<br>
              else<br>
                  p=p->left;<br>
         }<br>
         t->parent=q;<br>
         if(q->key<t->key)<br>
              q->right=t;<br>
         else<br>
              q->left=t;<br>
     }<br>
     insertfix(t);<br>
}<br>
void RBtree::insertfix(node *t)<br>
{<br>
     node *u;<br>
     if(root==t)<br>
     {<br>
         t->color='b';<br>
         return;<br>
     }<br>
     while(t->parent!=NULL&&t->parent->color=='r')<br>
     {<br>
           node *g=t->parent->parent;<br>
           if(g->left==t->parent)<br>
           {<br>
                        if(g->right!=NULL)<br>
                        {<br>
                              u=g->right;<br>
                              if(u->color=='r')<br>
                              {<br>
                                   t->parent->color='b';<br>
                                   u->color='b';<br>
                                   g->color='r';<br>
                                   t=g;<br>
                              }<br>
                        }<br>
                        else<br>
                        {<br>
                            if(t->parent->right==t)<br>
                            {<br>
                                 t=t->parent;<br>
                                 leftrotate(t);<br>
                            }<br>
                            t->parent->color='b';<br>
                            g->color='r';<br>
                            rightrotate(g);<br>
                        }<br>
           }<br>
           else<br>
           {<br>
                        if(g->left!=NULL)<br>
                        {<br>
                             u=g->left;<br>
                             if(u->color=='r')<br>
                             {<br>
                                  t->parent->color='b';<br>
                                  u->color='b';<br>
                                  g->color='r';<br>
                                  t=g;<br>
                             }<br>
                        }<br>
                        else<br>
                        {<br>
                            if(t->parent->left==t)<br>
                            {<br>
                                   t=t->parent;<br>
                                   rightrotate(t);<br>
                            }<br>
                            t->parent->color='b';<br>
                            g->color='r';<br>
                            leftrotate(g);<br>
                        }<br>
           }<br>
           root->color='b';<br>
     }<br>
}<br>

void RBtree::del()<br>
{<br>
     if(root==NULL)<br>
     {<br>
           cout<<"\nEmpty Tree." ;<br>
           return ;<br>
     }<br>
     int x;<br>
     cout<<"\nEnter the key of the node to be deleted: ";<br>
     cin>>x;<br>
     node *p;<br>
     p=root;<br>
     node *y=NULL;<br>
     node *q=NULL;<br>
     int found=0;<br>
     while(p!=NULL&&found==0)<br>
     {<br>
           if(p->key==x)<br>
               found=1;<br>
           if(found==0)<br>
           {<br>
                 if(p->key<x)<br>
                    p=p->right;<br>
                 else<br>
                    p=p->lef<br>;<br>
           }<br>
     }<br>
     if(found==0)<br>
     {<br>
            cout<<"\nElement Not Found.";<br>
            return ;<br>
     }<br>
     else<br>
     {<br>
         cout<<"\nDeleted Element: "<<p->key;<br>
         cout<<"\nColour: ";<br>
         if(p->color=='b')<br>
     cout<<"Black\n";<br>
    else<br>
     cout<<"Red\n";<br>

         if(p->parent!=NULL)<br>
               cout<<"\nParent: "<<p->parent->key;<br>
         else<br>
               cout<<"\nThere is no parent of the node.  ";<br>
         if(p->right!=NULL)<br>
               cout<<"\nRight Child: "<<p->right->key;<br>
         else<br>
               cout<<"\nThere is no right child of the node.  ";<br>
         if(p->left!=NULL)<br>
               cout<<"\nLeft Child: "<<p->left->key;<br>
         else<br>
               cout<<"\nThere is no left child of the node.  ";<br>
         cout<<"\nNode Deleted.";<br>
         if(p->left==NULL||p->right==NULL)<br>
              y=p;<br>
         else<br>
              y=successor(p);<br>
         if(y->left!=NULL)<br>
              q=y->left;<br>
         else<br>
         {<br>
              if(y->right!=NULL)<br>
                   q=y->right;<br>
              else<br>
                   q=NULL;<br>
         }<br>
         if(q!=NULL)<br>
              q->parent=y->parent;<br>
         if(y->parent==NULL)<br>
              root=q;<br>
         else<br>
         {<br>
             if(y==y->parent->left)<br>
                y->parent->left=q;<br>
             else<br>
                y->parent->right=q;<br>
         }<br>
         if(y!=p)<br>
         {<br>
             p->color=y->color;<br>
             p->key=y->key;<br>
         }<br>
         if(y->color=='b')<br>
             delfix(q);<br>
     }<br>
}<br>

void RBtree::delfix(node *p)<br>
{<br>
    node *s;<br>
    while(p!=root&&p->color=='b')<br>
    {<br>
          if(p->parent->left==p)<br>
          {<br>
                  s=p->parent->right;<br>
                  if(s->color=='r')<br>
                  {<br>
                         s->color='b';<br>
                         p->parent->color='r';<br>
                         leftrotate(p->parent);<br>
                         s=p->parent->right;<br>
                  }<br>
                  if(s->right->color=='b'&&s->left->color=='b')<br>
                  {<br>
                         s->color='r';<br>
                         p=p->parent;<br>
                  }<br>
                  else<br>
                  {<br>
                      if(s->right->color=='b')<br>
                      {<br>
                             s->left->color=='b';<br>
                             s->color='r';<br>
                             rightrotate(s);<br>
                             s=p->parent->right;<br>
                      }<br>
                      s->color=p->parent->color;<br>
                      p->parent->color='b';<br>
                      s->right->color='b';<br>
                      leftrotate(p->parent);<br>
                      p=root;<br>
                  }<br>
          }<br>
          else<br>
          {<br>
                  s=p->parent->left;<br>
                  if(s->color=='r')<br>
                  {<br>
                        s->color='b';<br>
                        p->parent->color='r';<br>
                        rightrotate(p->parent);<br>
                        s=p->parent->left;<br>
                  }<br>
                  if(s->left->color=='b'&&s->right->color=='b')<br>
                  {<br>
                        s->color='r';<br>
                        p=p->parent;<br>
                  }<br>
                  else<br>
                  {<br>
                        if(s->left->color=='b')<br>
                        {<br>
                              s->right->color='b';<br>
                              s->color='r';<br>
                              leftrotate(s);<br>
                              s=p->parent->left;<br>
                        }<br>
                        s->color=p->parent->color;<br>
                        p->parent->color='b';<br>
                        s->left->color='b';<br>
                        rightrotate(p->parent);<br>
                        p=root;<br>
                  }<br>
          }<br>
       p->color='b';<br>
       root->color='b';<br>
    }<br>
}<br>

void RBtree::leftrotate(node *p)<br>
{<br>
     if(p->right==NULL)<br>
           return ;<br>
     else<br>
     {<br>
           node *y=p->right;<br>
           if(y->left!=NULL)<br>
           {<br>
                  p->right=y->left;<br>
                  y->left->parent=p;<br>
           }<br>
           else<br>
                  p->right=NULL;<br>
           if(p->parent!=NULL)<br>
                y->parent=p->parent;<br>
           if(p->parent==NULL)<br>
                root=y;<br>
           else<br>
           {<br>
               if(p==p->parent->left)<br>
                       p->parent->left=y;<br>
               else<br>
                       p->parent->right=y;<br>
           }<br>
           y->left=p;<br>
           p->parent=y;<br>
     }<br>
}<br>
void RBtree::rightrotate(node *p)<br>
{<br>
     if(p->left==NULL)<br>
          return ;<br>
     else<br>
     {<br>
         node *y=p->left;<br>
         if(y->right!=NULL)<br>
         {<br>
                  p->left=y->right;<br>
                  y->right->parent=p;<br>
         }<br>
         else<br>
                 p->left=NULL;<br>
         if(p->parent!=NULL)<br>
                 y->parent=p->parent;<br>
         if(p->parent==NULL)<br>
               root=y;<br>
         else<br>
         {<br>
             if(p==p->parent->left)<br>
                   p->parent->left=y;<br>
             else<br>
                   p->parent->right=y;<br>
         }<br>
         y->right=p;<br>
         p->parent=y;<br>
     }<br>
}<br>

node* RBtree::successor(node *p)<br>
{<br>
      node *y=NULL;<br>
     if(p->left!=NULL)<br>
     {<br>
         y=p->left;<br>
         while(y->right!=NULL)<br>
              y=y->right;<br>
     }<br>
     else<br>
     {<br>
         y=p->right;<br>
         while(y->left!=NULL)<br>
              y=y->left;<br>
     }<br>
     return y;<br>
}<br>

void RBtree::disp()<br>
{<br>
     display(root);<br>
}<br>
void RBtree::display(node *p)<br>
{<br>
     if(root==NULL)<br>
     {<br>
          cout<<"\nEmpty Tree.";<br>
          return ;<br>
     }<br>
     if(p!=NULL)<br>
     {<br>
                cout<<"\n\t NODE: ";<br>
                cout<<"\n Key: "<<p->key;<br>
                cout<<"\n Colour: ";<br>
    if(p->color=='b')<br>
     cout<<"Black";<br>
    else<br>
     cout<<"Red";<br>
                if(p->parent!=NULL)<br>
                       cout<<"\n Parent: "<<p->parent->key;<br>
                else<br>
                       cout<<"\n There is no parent of the node.  ";<br>
                if(p->right!=NULL)<br>
                       cout<<"\n Right Child: "<<p->right->key;<br>
                else<br>
                       cout<<"\n There is no right child of the node.  ";<br>
                if(p->left!=NULL)<br>
                       cout<<"\n Left Child: "<<p->left->key;<br>
                else<br>
                       cout<<"\n There is no left child of the node.  ";<br>
                cout<<endl;<br>
    if(p->left)<br>
    {<br>
                 cout<<"\n\nLeft:\n";<br>
     display(p->left);<br>
    }<br>
    
    if(p->right)<br>
    {<br>
     cout<<"\n\nRight:\n";<br>
                 display(p->right);<br>
    }<br>
    
     }<br>
}<br>
void RBtree::search()<br>
{<br>
     if(root==NULL)<br>
     {<br>
           cout<<"\nEmpty Tree\n" ;<br>
           return  ;<br>
     }<br>
     int x;<br>
     cout<<"\n Enter key of the node to be searched: ";<br>
     cin>>x;<br>
     node *p=root;<br>
     int found=0;<br>
     while(p!=NULL&& found==0)<br>
     {<br>
            if(p->key==x)<br>
                found=1;<br>
            if(found==0)<br>
            {<br>
                 if(p->key<x)<br>
                      p=p->right;<br>
                 else<br>
                      p=p->left;<br>
            }<br>
     }<br>
     if(found==0)<br>
          cout<<"\nElement Not Found.";<br>
     else<br>
     {<br>
                cout<<"\n\t FOUND NODE: ";<br>
                cout<<"\n Key: "<<p->key;<br>
                cout<<"\n Colour: ";<br>
    if(p->color=='b')<br>
     cout<<"Black";<br>
    else<br>
     cout<<"Red";<br>
                if(p->parent!=NULL)<br>
                       cout<<"\n Parent: "<<p->parent->key;<br>
                else<br>
                       cout<<"\n There is no parent of the node.  ";<br>
                if(p->right!=NULL)<br>
                       cout<<"\n Right Child: "<<p->right->key;<br>
                else<br>
                       cout<<"\n There is no right child of the node.  ";<br>
                if(p->left!=NULL)<br>
                       cout<<"\n Left Child: "<<p->left->key;<br>
                else<br>
                       cout<<"\n There is no left child of the node.  ";<br>
                cout<<endl;<br>

     }<br>
}<br>
int main()<br>
{
    int ch,y=0;<br>
    RBtree obj;<br>
    do<br>
    {<br>
                cout<<"\n\t RED BLACK TREE " ;<br>
                cout<<"\n 1. Insert in the tree ";<br>
                cout<<"\n 2. Delete a node from the tree";<br>
                cout<<"\n 3. Search for an element in the tree";<br>
                cout<<"\n 4. Display the tree ";<br>
                cout<<"\n 5. Exit " ;<br>
                cout<<"\nEnter Your Choice: ";<br>
                cin>>ch;<br>
                switch(ch)<br>
                {<br>
                          case 1 : obj.insert();<br>
                                   cout<<"\nNode Inserted.\n";<br>
                                   break;<br>
                          case 2 : obj.del();<br>
                                   break;<br>
                          case 3 : obj.search();<br>
                                   break;<br>
                          case 4 : obj.disp();<br>
                                   break;<br>
                          case 5 : y=1;<br>
                                   break;<br>
                          default : cout<<"\nEnter a Valid Choice.";<br>
                }<br>
                cout<<endl;<br>

    }while(y!=1);<br>
    return 1;<br>
}<br>
	
	![image](https://user-images.githubusercontent.com/97940332/162895068-4bdf1bae-bc98-4a8c-8c9e-4bafe2c6ccf7.png)
	![image](https://user-images.githubusercontent.com/97940332/162895201-9b75ad93-894f-421f-ad17-41632632189d.png)
	![image](https://user-images.githubusercontent.com/97940332/162895297-737bed82-c8c5-47b3-ac96-1b1df5e1a151.png)
	![image](https://user-images.githubusercontent.com/97940332/162895402-01ef2c26-43c0-4cae-ac76-b87a0570aabf.png)

			      
 **//Program to implementing Doubly LL**
#include<iostream><br>
#include<cstdio><br>
#include<cstdlib><br>
using namespace std;<br>
struct node<br>
{<br>
    int info;<br>
    struct node *next;<br>
    struct node *prev;<br>
}*start;<br>
class double_llist<br>
{<br>
    public:<br>
        void create_list(int value);<br>
        void add_begin(int value);<br>
        void add_after(int value, int position);<br>
        void delete_element(int value);<br>
        void search_element(int value);<br>
        void display_dlist();<br>
        void count();<br>
        void reverse();<br>
        double_llist()<br>
        {<br>
            start = NULL;  <br>
        }<br>
};<br>
 int main()<br>
{<br>
    int choice, element, position;<br>
    double_llist dl;<br>
    while (1)<br>
    {<br>
        cout<<endl<<"----------------------------"<<endl;<br>
        cout<<endl<<"Operations on Doubly linked list"<<endl;<br>
        cout<<endl<<"----------------------------"<<endl; <br>       
        cout<<"1.Create Node"<<endl;<br>
        cout<<"2.Add at begining"<<endl;<br>
        cout<<"3.Add after position"<<endl;<br>
        cout<<"4.Delete"<<endl;<br>
        cout<<"5.Display"<<endl;<br>
        cout<<"6.Count"<<endl;<br>
        cout<<"7.Reverse"<<endl;<br>
        cout<<"8.Quit"<<endl;<br>
        cout<<"Enter your choice : ";<br>
        cin>>choice;<br>
        switch ( choice )<br>
        {<br>
        case 1:<br>
            cout<<"Enter the element: ";<br>
            cin>>element;<br>
            dl.create_list(element);<br>
            cout<<endl;<br>
            break;<br>
        case 2:<br>
            cout<<"Enter the element: ";<br>
            cin>>element;<br>
            dl.add_begin(element);<br>
            cout<<endl;<br>
            break;<br>
        case 3:<br>
            cout<<"Enter the element: ";<br>
            cin>>element;<br>
            cout<<"Insert Element after postion: ";<br>
            cin>>position;<br>
            dl.add_after(element, position);<br><br>
            cout<<endl;<br>
            break;<br>
        case 4:<br>
            if (start == NULL)<br>
            {  <br>                    
                cout<<"List empty,nothing to delete"<<endl;  <br>
                break;<br>
            }<br>
            cout<<"Enter the element for deletion: ";<br>
            cin>>element;<br>
            dl.delete_element(element);<br>
            cout<<endl;<br>
            break;<br>
        case 5:<br>
            dl.display_dlist();<br>
            cout<<endl;<br>
            break;<br>
        case 6:<br>
            dl.count();<br>
            break;    <br>
        case 7:<br>
            if (start == NULL)<br>
            {<br>
                cout<<"List empty,nothing to reverse"<<endl;<br>
                break;<br>
            }<br>
            dl.reverse();<br>
            cout<<endl;<br>
            break;<br>
        case 8:<br>
            exit(1);<br>
        default:<br>
            cout<<"Wrong choice"<<endl;<br>
        }<br>
    }<br>
    return 0;<br>
}<br>
 void double_llist::create_list(int value)<br>
{<br>
    struct node *s, *temp;<br>
    temp = new(struct node);<br>
    temp->info = value;<br>
    temp->next = NULL;<br>
    if (start == NULL)<br>
    {<br>
        temp->prev = NULL;<br>
        start = temp;<br>
    }<br>
    else<br>
    {<br>
        s = start;<br>
        while (s->next != NULL)<br>
            s = s->next;<br>
        s->next = temp;<br>
        temp->prev = s;<br>
    }<br>
}<br>
 void double_llist::add_begin(int value)<br>
{<br>
    if (start == NULL)<br>
    {<br>
        cout<<"First Create the list."<<endl;<br>
        return;<br>
    }<br>
    struct node *temp;<br>
    temp = new(struct node);<br>
    temp->prev = NULL;<br>
    temp->info = value;<br>
    temp->next = start;<br>
    start->prev = temp;<br>
    start = temp;<br>
    cout<<"Element Inserted"<<endl;<br>
}<br>
void double_llist::add_after(int value, int pos)<br>
{<br>
    if (start == NULL)<br>
    {<br>
        cout<<"First Create the list."<<endl;<br>
        return;<br>
    }<br>
    struct node *tmp, *q;<br>
    int i;<br>
    q = start;<br>
    for (i = 0;i < pos - 1;i++)<br>
    {<br>
        q = q->next;<br>
        if (q == NULL)<br>
        {<br>
            cout<<"There are less than ";<br>
            cout<<pos<<" elements."<<endl;<br>
            return;<br>
        }<br>
    }<br>
    tmp = new(struct node);<br>
    tmp->info = value;<br>
    if (q->next == NULL)<br>
    {<br>
        q->next = tmp;<br>
        tmp->next = NULL;<br>
        tmp->prev = q;   <br>   
    }<br>
    else<br>
    {<br>
        tmp->next = q->next;<br>
        tmp->next->prev = tmp;<br>
        q->next = tmp;<br>
        tmp->prev = q;<br>
    }<br>
    cout<<"Element Inserted"<<endl;<br>
}<br>
 void double_llist::delete_element(int value)<br>
{<br>
    struct node *tmp, *q;<br>
        if (start->info == value)<br>
    {<br>
        tmp = start;<br>
        start = start->next;  <br>
        start->prev = NULL;<br>
        cout<<"Element Deleted"<<endl;<br>
        free(tmp);<br>
        return;<br>
    }<br>
    q = start;<br>
    while (q->next->next != NULL)<br>
    {  <br>
               if (q->next->info == value) <br> 
        {
            <br>tmp = q->next;<br>
            q->next = tmp->next;<br>
            tmp->next->prev = q;<br>
            cout<<"Element Deleted"<<endl;<br>
            free(tmp);<br>
            return;<br>
        }<br>
        q = q->next;<br>
    }<br>
        if (q->next->info == value)    <br>
    {<br>
        tmp = q->next;<br>
        free(tmp);<br>
        q->next = NULL;<br>
        cout<<"Element Deleted"<<endl;<br>
        return;<br>
    }<br>
    cout<<"Element "<<value<<" not found"<<endl;<br>
}<br>
 void double_llist::display_dlist()<br>
{<br>
    struct node *q;<br>
    if (start == NULL)<br>
    {<br>
        cout<<"List empty,nothing to display"<<endl;<br>
        return;<br>
    }<br>
    q = start;<br>
    cout<<"The Doubly Link List is :"<<endl;<br>
    while (q != NULL)<br>
    {<br>
        cout<<q->info<<" <-> ";<br>
        q = q->next;<br>
    }<br>
    cout<<"NULL"<<endl;<br>
}<br>
 void double_llist::count()<br>
{<br>
    struct node *q = start;<br>
    int cnt = 0;<br>
    while (q != NULL)<br>
    {<br>
        q = q->next;<br>
        cnt++;<br>
    }<br>
    cout<<"Number of elements are: "<<cnt<<endl;<br>
}<br>
 void double_llist::reverse()<br>
{<br>
    struct node *p1, *p2;<br>
    p1 = start;<br>
    p2 = p1->next;<br>
    p1->next = NULL;<br>
    p1->prev = p2;<br>
    while (p2 != NULL)<br>
    {<br>
        p2->prev = p2->next;<br>
        p2->next = p1;<br>
        p1 = p2;<br>
        p2 = p2->prev;<br>
    }<br>
    start = p1;<br>
    cout<<"List Reversed"<<endl;<br>
}<br>
	
	**OUTPUT:**
	
	![image](https://user-images.githubusercontent.com/97940332/163162920-824c44be-caa5-4bce-9570-a3168e5a0f7c.png)
![image](https://user-images.githubusercontent.com/97940332/163163405-f9aef490-968b-4581-9829-2fa5e3cb93d5.png)
![image](https://user-images.githubusercontent.com/97940332/163163513-14a0f7ce-f628-4bfd-a030-52501f29529d.png)
![image](https://user-images.githubusercontent.com/97940332/163163578-d7ac3363-f8b8-47e1-90dc-e7f935336fdb.png)
![image](https://user-images.githubusercontent.com/97940332/163163627-978503d2-742e-4b4e-87d4-f0977674c6ab.png)

**//N-Queens problem**
	
	
//program to solve the n queen problem <br>
//grid[][] is represent the 2-d array with value(0 and 1) for grid[i][j]=1 means queen i are placed at j column.<br>
//we can take any number of queen , for this time we take the atmost 10 queen (grid[10][10]).<br>
#include<iostream><br>
using namespace std;<br>
int grid[10][10];<br>

//print the solution<br>
void print(int n)<br> {<br>
    for (int i = 0;i <= n-1; i++)<br> {<br>
        for (int j = 0;j <= n-1; j++)<br> {<br>
            
                cout <<grid[i][j]<< " ";<br>
            
        }<br>
        cout<<endl;<br>
    }<br>
    cout<<endl;<br>
    cout<<endl;<br>
}<br>

//function for check the position is safe or not<br>
//row is indicates the queen no. and col represents the possible positions<br>
bool isSafe(int col, int row, int n)<br> {<br>
  //check for same column<br>
    for (int i = 0; i < row; i++) <br>{<br>
        if (grid[i][col])<br> {<br>
            return false;<br>
        }<br>
    }<br>
    //check for upper left diagonal<br>
    for (int i = row,j = col;i >= 0 && j >= 0; i--,j--) <br>{<br>
        if (grid[i][j])<br> {<br>
            return false;<br>
        }<br>
    }<br>
    //check for upper right diagonal<br>
    for (int i = row, j = col; i >= 0 && j < n; j++, i--) <br>{<br>
        if (grid[i][j]) <br>{<br>
            return false;<br>
        }<br>
    }<br>
    return true;<br>
}<br>

//function to find the position for each queen<br>
//row is indicates the queen no. and col represents the possible positions<br>
bool solve (int n, int row)<br> {<br>
    if (n == row)<br> {<br>
        print(n);<br>
        return true;<br>
    }<br>
    //variable res is use for possible backtracking <br>
    bool res = false;<br>
    for (int i = 0;i <=n-1;i++)<br> {<br>
        if (isSafe(i, row, n))<br> {<br>
            grid[row][i] = 1;<br>
            //recursive call solve(n, row+1) for next queen (row+1)<br>
            res = solve(n, row+1) || res;//if res ==false then backtracking will occur <br>
            //by assigning the grid[row][i] = 0<br>
            
            grid[row][i] = 0;<br>
        }<br>
    }<br>
    return res;<br>
}<br>

int main()<br>
{<br>
  ios_base::sync_with_stdio(false);<br>
    cin.tie(NULL);<br>
        int n;<br>
        cout<<"Enter the number of queen"<<endl;<br>
        cin >> n;<br>
        for (int i = 0;i < n;i++)<br> {<br>
            for (int j = 0;j < n;j++)<br> {<br>
                grid[i][j] = 0;<br>
            }<br>
        }<br>
        bool res = solve(n, 0);<br>
        if(res == false)<br> {<br>
            cout << -1 << endl; //if there is no possible solution<br>
        }<br> else <br>{<br>
            cout << endl;<br>
        }<br>
  return 0;<br>
}<br><br><br>
	
**OUTPUT:**
	
![image](https://user-images.githubusercontent.com/97940332/163940535-f540ba99-6ec1-493e-8449-9ef10c847c79.png)



	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	

	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	

	
	
	
	
	
	
	
	
	
	
	


	
	

		 


		


   
   
