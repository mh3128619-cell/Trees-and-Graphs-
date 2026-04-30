class TrieNode:
    def __init__(self):
        self.children = {}
        self.count = 0

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for ch in word:
            if ch not in node.children:
                node.children[ch] = TrieNode()
            node = node.children[ch]
        node.count += 1

    def get_frequency(self, word):
        node = self.root
        for ch in word:
            if ch not in node.children:
                return 0
            node = node.children[ch]
        return node.count

trie = Trie()
trie.insert("apple")
trie.insert("apple")
trie.insert("apply")

print(trie.get_frequency("apple"))
print(trie.get_frequency("apply"))
print(trie.get_frequency("app"))
print(trie.get_frequency("banana"))
