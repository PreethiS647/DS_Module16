# Ex4c B-Tree
## DATE: 9-4-25
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1.	Start
2.	Try to delete the item from the node using delValFromNode. If not found, print "Not present" and return.
3.	If the node's count is 0 after deletion, set tmp to the current node and update myNode to its first linker child.
4.	Free the tmp node.
5.	Update the global root to the new myNode.
6.	Return after deletion.
7.	End


## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: Preethi S
RegisterNumber: 212223230157 
*/

struct BTreeNode{
int item[MAX+1], count;
struct BTreeNode*linker[MAX+1];
};

struct BTreeNode*root;*/
voiddelete(int item, struct BTreeNode*myNode) { struct BTreeNode*tmp; if(!delValFromNode(item, myNode)){ printf("Not present\n");
return;
} else{
if(myNode->count ==0) { tmp = myNode;
myNode=myNode->linker[0]; free(tmp);
}
}
root=myNode; return;
}

```

## Output:

![image](https://github.com/user-attachments/assets/84ccfe9b-0d72-406b-a9d4-b9b8b303d93d)


## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
