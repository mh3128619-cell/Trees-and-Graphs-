class TrieNode:
    def __init__(self):
        self.children = {}
        self.count = 0
        self.is_end_of_word = False

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                node.children[char] = TrieNode()
            node = node.children[char]
            node.count += 1
        node.is_end_of_word = True

    def count_words_with_prefix(self, prefix):
        node = self.root
        for char in prefix:
            if char not in node.children:
                return 0
            node = node.children[char]
        return node.count

trie = Trie()
words = ["Ali", "Aliaa", "Apple", "Amr"]
for w in words:
    trie.insert(w)

print(f"Count for 'Al': {trie.count_words_with_prefix('Al')}")
print(f"Count for 'Ap': {trie.count_words_with_prefix('Ap')}")
print(f"Count for 'A': {trie.count_words_with_prefix('A')}")
