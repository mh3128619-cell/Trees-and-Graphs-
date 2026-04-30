class Node:
    def __init__(self, key):
        self.val = key
        self.left = None
        self.right = None

def find_min_node(node):
    current = node
    while current.left is not None:
        current = current.left
    return current

def delete_node(root, key):
    if root is None:
        return root

    if key < root.val:
        root.left = delete_node(root.left, key)
    elif key > root.val:
        root.right = delete_node(root.right, key)
    else:

        if root.left is None:
            return root.right
        elif root.right is None:
            return root.left

        temp = find_min_node(root.right)
        
        root.val = temp.val
        
        root.right = delete_node(root.right, temp.val)

    return root

def print_inorder(root):
    if root:
        print_inorder(root.left)
        print(root.val, end=" ")
        print_inorder(root.right)

root = Node(10)
root.right = Node(15)
root.right.left = Node(12)
root.right.right = Node(20)

print("Tree before deletion (In-order):")
print_inorder(root)  # Expected: 10 12 15 20

root = delete_node(root, 15)

print("\n\nTree after deleting 15:")
print_inorder(root) 
