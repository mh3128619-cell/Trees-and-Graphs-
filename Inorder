class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

def search(root, key):
    if root is None or root.val == key:
        return root
    if root.val < key:
        return search(root.right, key)
    return search(root.left, key)

def print_inorder(root):
    if root:
        print_inorder(root.left)
        print(root.val, end=" ")
        print_inorder(root.right)

root = Node(10)
root.left = Node(5)
root.right = Node(15)
root.left.left = Node(2)
root.right.right = Node(20)

print("In-order Traversal (Sorted):")
print_inorder(root) 
print("\n" + "-"*20)

result_20 = search(root, 20)
print("Searching for 20:", "Found!" if result_20 else "Not Found")
