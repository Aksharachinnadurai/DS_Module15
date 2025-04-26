# Ex1 NO:3(A) Tree Representation and Traversal
## DATE:15/3/25
## AIM:
To write a C function to perform post order traversal of a binary tree.

## Algorithm
1. Start
2. Define a function display_postorder() that takes a pointer to the root node of the tree.
3. Check if the current node (root_node) is not null.
4. Recursively call display_postorder() for the left child of the current node.
5. Recursively call display_postorder() for the right child of the current node.
6. After visiting both children, print the value of the current node.
7. End
## Program:
```
/*
Program to perform post order traversal of a binary tree.
Developed by:AKSHARA C 
RegisterNumber:  212223220004
*/
```
```
structnode{ 
int key;
struct node*left, *right;
};
struct node* insert(struct node* node, int key)
{
if(node==NULL)
{
struct node*node=(struct node*)malloc(sizeof(struct node)); 
node->key=key;
node->left=NULL; 
node->right=NULL; 
return node;
}
else
{
struct node* cur; 
if(key<=node->key)
{
cur=insert(node->left,key); 
node->left=cur;
}
else
{
cur=insert(node->right,key); 
node->right=cur;
}
returnnode;
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/55601004-5f09-457f-9fe4-c1ba648bae10)

## Result:
Thus, the function to perform post order traversal of a binary tree is implemented successfully
