def rebalance_left_right(self, root, key, balance):
    if balance > 1 and key > root.left.val:
        root.left = self.left_rotate(root.left)
        return self.right_rotate(root)
    return root

print("Left-Right (Zigzag) rebalancing logic is ready.")
