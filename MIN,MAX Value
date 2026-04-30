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

def find_min(root):
    if root is None:
        return None
    current = root
    while current.left is not None:
        current = current.left
    return current.val

def find_max(root):
    if root is None:
        return None
    current = root
    while current.right is not None:
        current = current.right
    return current.val

root = Node(10)
root.left = Node(5)
root.right = Node(15)
root.left.left = Node(2)
root.right.right = Node(20)

print("In-order Traversal (Sorted):")
print_inorder(root)
print("\n" + "-"*20)

print(f"Minimum value in BST: {find_min(root)}")
print(f"Maximum value in BST: {find_max(root)}")

search_key = 20
result = search(root, search_key)
print(f"Searching for {search_key}:", "Found!" if result else "Not Found")
