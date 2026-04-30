def get_height(root):
    if root is None:
        return -1
    
    left_height = get_height(root.left)
    right_height = get_height(root.right)

    return max(left_height, right_height) + 1

print(f"Height of the tree: {get_height(root)}")
