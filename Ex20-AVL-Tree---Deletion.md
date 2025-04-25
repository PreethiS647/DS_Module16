# Ex2e AVL Tree - Deletion
## DATE:18-4-25
## AIM:
To write a C function to delete an element from an AVL Tree.
## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Preethi S
RegisterNumber:  212223230157
*/


node * Delete(node *T,int x)
{
node *p; if(T==NULL)
{
return NULL;
}
else
if(x > T->data) // insert in right subtree
{
T->right=Delete(T->right,x); if(BF(T)==2)
{
if(BF(T->left)>=0) T=LL(T);
else T=LR(T);
}}
else
if(x<T->data)
{
T->left=Delete(T->left,x);
if(BF(T)==-2) //Rebalance during windup
{
if(BF(T->right)<=0) T=RR(T);
else T=RL(T);
}}
else
 
{
//data to be deleted is found if(T->right!=NULL)
{ //delete its inorder succesor p=T->right;
while(p->left!= NULL) p=p->left;
T->data=p->data;
T->right=Delete(T->right,p->data); if(BF(T)==2)//Rebalance during windup
{
if(BF(T->left)>=0) T=LL(T);
else T=LR(T);}}
else
return(T->left);
}
T->ht=height(T); return(T);
}





```

## Output:

![image](https://github.com/user-attachments/assets/cbf06bf8-69eb-416d-87aa-59ee91ced497)


## Result:
Thus, the C program to delete an element from an AVL Tree is implemented successfully.
