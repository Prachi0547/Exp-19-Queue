# Exp-19-Queue
# Aim
To learn queue in c++.
# Problem Statement
Write a program to dequeue & enqueue in c++.
# Software Used
VS Code and c++ online compiler.
# Theory
A queue is a linear data structure that follows the First In, First Out (FIFO) principle, meaning that the first element added to the queue is the first one to be removed. This structure is commonly used in scenarios like task scheduling, buffering, and breadth-first search algorithms.

The Basic Operations:
Enqueue (Adds an element to the end of the queue.) ,
Dequeue (Removes the element from the front of the queue.) ,
Front/Peek (Retrieves the element at the front of the queue without removing it.) ,
IsEmpty (Checks whether the queue is empty.)

# Program Code
```
//Dequeue & Enqueue

#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Queue{
    int rear, front, ar[size];
    public:
    Queue(){
        rear = -1;
        front = -1;
        ar[0]=0;
    }
    void enqueue(int);
    int dequeue();
    void disp();
};
void Queue :: enqueue(int num){
    if (rear == (size+1)){
        cout<<"Queue is full"<<endl;
    }
    else{
        if(front == -1){
            ar[++front]=num;
            rear++;
        }
        else{
            ar[++rear]=num;
        }
    }

    }
int Queue ::dequeue(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Queue is empty"<<endl;
        return ERROR;
    }
    else{
        int val = ar[front++];
        return val;
    }
}
void Queue :: disp(){
    if(front ==-1 || front ==(rear+1)){
        cout<<"Quee=ue is empty"<<endl;
        return;
    }
    else{
        int i = front ;
        while (i!=(rear+1)){
            cout<<ar[i];
            i++;
        }
    }
}

int main(){
        Queue q1;
        q1.enqueue(4);
        q1.enqueue(8);
        q1.enqueue(3);
        q1.disp();
        int val = q1.dequeue();
        cout<<endl<<"Deleted element: "<<val<<endl;
        q1.disp();
}
```
# Output
![image](https://github.com/user-attachments/assets/97a32477-47fd-418b-9562-e4866febcef0)

# Conclusion
We learnt how to dequeue & enqueue in c++.
