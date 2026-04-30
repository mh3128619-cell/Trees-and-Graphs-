class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

def insert(root, key):

    if root is None:
        return Node(key)
    
    if key < root.val:
        root.left = insert(root.left, key)
    
    elif key > root.val:
        root.right = insert(root.right, key)
        
    return root

def print_inorder(root):
    if root:
        print_inorder(root.left)
        print(root.val, end=" ")
        print_inorder(root.right)

root = None
values = [10, 5, 15, 2, 20]

for val in values:
    root = insert(root, val)

print("BST In-order Traversal (Should be sorted):")
print_inorder(root)
