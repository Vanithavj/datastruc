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

	
3.//C++ program to implement addition of 2 Arrays.
	
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
	
	
	
4.//C++ Program to implement reverse order of array elements
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





		 


		


   
   
