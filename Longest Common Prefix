class TrieNode:
    def __init__(self):
        self.children = {}
        self.count = 0
        self.is_end_of_word = False

class Trie:
    def __init__(self):
        self.root = TrieNode()
        self.total_words = 0

    def insert(self, word):
        if not word:
            return
        node = self.root
        self.total_words += 1
        for char in word:
            if char not in node.children:
                node.children[char] = TrieNode()
            node = node.children[char]
            node.count += 1
        node.is_end_of_word = True

    def longest_common_prefix(self):
        node = self.root
        prefix = ""
        while len(node.children) == 1 and not node.is_end_of_word:
            char = list(node.children.keys())[0]
            next_node = node.children[char]
            if next_node.count == self.total_words:
                prefix += char
                node = next_node
            else:
                break
        return prefix

trie = Trie()
words = ["flower", "flow", "flight"]
for w in words:
    trie.insert(w)

print(f"Longest common prefix: '{trie.longest_common_prefix()}'")
