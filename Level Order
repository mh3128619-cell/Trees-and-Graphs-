def print_level_order(root):
    if not root:
        return
    
    queue = [root]
    while queue:
        level_size = len(queue)
        for _ in range(level_size):
            node = queue.pop(0)
            print(node.val, end=" ")
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)
        print() 

print("Level-order traversal of the current AVL tree:")
print_level_order(root)
