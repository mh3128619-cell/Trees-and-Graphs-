class TrieNode:
    def __init__(self):
        self.children = {}
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
        node.is_end_of_word = True

    def search(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                return False
            node = node.children[char]
        return node.is_end_of_word

my_trie = Trie()
words = ["Ali", "Amr", "Aliaa", "Apple"]

for w in words:
    my_trie.insert(w)

print(f"Is 'Apple' found? {my_trie.search('Apple')}")
print(f"Is 'Amr' found? {my_trie.search('Amr')}")
print(f"Is 'Ahmed' found? {my_trie.search('Ahmed')}")
