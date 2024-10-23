# DFS.py
class TreeNode:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None


def dfs(root):
    if root:
        print(root.value, end=' ')
        dfs(root.left)
        dfs(root.right)

def post_order(root):
    if not root:
        return
    post_order(root.left)
    post_order(root.right)
    print(root.value, end=" ")



if __name__ == "__main__":
    root = TreeNode(1)
    root.left = TreeNode(2)
    root.right = TreeNode(3)
    root.left.left = TreeNode(4)
    root.left.right = TreeNode(5)

    print("DFS traversal of the tree:")
    dfs(root)

    
