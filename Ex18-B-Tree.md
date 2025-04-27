# Ex18 B-Tree
## DATE : 26.04.2025
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1. Start and try deleting the item using delValFromNode.
2. If not found, print "Not present" and return.
3. If node's count is 0, set tmp = myNode and update myNode to its first linker child.
4. Free tmp and update the global root.
5. Return after deletion and end.

## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: vinodhini k
RegisterNumber:  212223230245
*/
*structBTreeNode{
int item[MAX+1], count;
structBTreeNode*linker[MAX +1];
};
structBTreeNode*root;*/
void delete(int item,structBTreeNode*myNode) {
structBTreeNode*tmp;
if(!delValFromNode(item,myNode)) {
printf("Not present\n");
return;
} else {
if(myNode->count ==0) {
tmp = myNode;
myNode=myNode->linker[0];
free(tmp);
}
}
root=myNode;
return;
}
```

## Output:

![image](https://github.com/user-attachments/assets/7c1a07ec-9992-4dda-8e46-03c28cfe9e41)


## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
