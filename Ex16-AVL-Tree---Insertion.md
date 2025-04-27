# Ex16 AVL Tree - Insertion
## DATE : 26.04.2025
## AIM:
To write a C function to insert the elements in an AVL Tree.

## Algorithm
1. Start; if node is NULL, create a new node with value x.
2. Insert x into left or right subtree recursively based on comparison.
3. Update height and calculate balance factor (BF).
4. If BF is -2 or 2, perform appropriate rotation (RR, RL, LL, LR).
5. Return new root after balancing and end.

## Program:
```
/*
Program to insert the elements in an AVL Tree
Developed by: vinodhini k
RegisterNumber: 212223230245
*/
node* insert(node*T,int x)
{
if(T==NULL)
{
T=(node*)malloc(sizeof(node));
T->data=x;
T->left=NULL;
T->right=NULL;
}
else
if(x>T->data)
{
T->right=insert(T->right,x);
if(BF(T)==-2)
{
if(x>T->right->data)
T=RR(T);
else
T=RL(T);
}
}
else
if(x<T->data)
{
T->left=insert(T->left,x);
if(BF(T)==2)
{
if(x<T->left->data)
T=LL(T);
else
T=LR(T);
}
}
T->ht=height(T);
return(T);
}

```

## Output:

![image](https://github.com/user-attachments/assets/adee5ec8-c082-43db-bbf3-5c68e5e2eb44)


## Result:
Thus, the function to insert the elements in an AVL Tree is implemented successfully in C programming language.
