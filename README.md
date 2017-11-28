#include<iostream>
using namespace std;
struct student
{
	char name[50];
	char num[15];
	int age;
	struct student *next;
};
int main()
{
	 struct student *p,*q,*head;
	 int s=1;
	 head=new student;
	 q=head;
	 while(cout<<"1or2"<<endl,cin>>s,s==1)
	 {
	 	p=new student;
	 	q->next=p;
	 	q=p;
	 	cin>>p->name;
	 	cin>>p->num;
	 	cin>>p->age;
	 	p->next=NULL;
	 }
	 p=head;
	 while(p!=NULL)
	 {
	 	cout<<p->name<<" "<<p->num<<" "<<p->age<<endl;
	 	p=p->next;
	 }
}
