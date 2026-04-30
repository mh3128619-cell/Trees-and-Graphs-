def search(root, key):

    if root is None or root.val == key:
        return root
    
    if root.val < key:
        return search(root.right, key)
    
    return search(root.left, key)

result_20 = search(root, 20)
result_100 = search(root, 100)

print("Searching for 20:", "Found!" if result_20 else "Not Found")
print("Searching for 100:", "Found!" if result_100 else "Not Found")
