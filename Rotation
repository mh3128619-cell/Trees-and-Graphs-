class Node:
    def __init__(self, key):
        self.val = key
        self.left = None
        self.right = None
        self.height = 1

def get_height(node):
    if not node:
        return 0
    return node.height

def left_rotate(z):
    """
    Performs a left rotation on node z.
    y becomes the new root of this subtree.
    """
    y = z.right
    T2 = y.left

    y.left = z
    z.right = T2

    z.height = 1 + max(get_height(z.left), get_height(z.right))
    y.height = 1 + max(get_height(y.left), get_height(y.right))

    return y

root = Node(10)
root.right = Node(15)
root.right.right = Node(20)

print("Original Root:", root.val)
new_root = left_rotate(root)
print("New Root after Left Rotation:", new_root.val)
print("New Left Child:", new_root.left.val)
print("New Right Child:", new_root.right.val)
