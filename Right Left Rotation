def rebalance_right_left(self, root, key, balance):
    if balance < -1 and key < root.right.val:
        root.right = self.right_rotate(root.right)
        return self.left_rotate(root)
    return root

print("Right-Left zigzag rebalancing logic is ready")
