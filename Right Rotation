def get_balance(node):
    if not node:
        return 0
    return get_height(node.left) - get_height(node.right)

def right_rotate(y):
    x = y.left
    T2 = x.right

    x.right = y
    y.left = T2

    y.height = 1 + max(get_height(y.left), get_height(y.right))
    x.height = 1 + max(get_height(x.left), get_height(x.right))

    return x

def rebalance(root, key):
    balance = get_balance(root)

    if balance > 1 and key < root.left.val:
        return right_rotate(root)

    if balance < -1 and key > root.right.val:
        return left_rotate(root)

    if balance > 1 and key > root.left.val:
        root.left = left_rotate(root.left)
        return right_rotate(root)

    if balance < -1 and key < root.right.val:
        root.right = right_rotate(root.right)
        return left_rotate(root)

    return root

print("AVL balancing logic is ready.")
