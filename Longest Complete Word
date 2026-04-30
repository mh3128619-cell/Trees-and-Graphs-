class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for ch in word:
            if ch not in node.children:
                node.children[ch] = TrieNode()
            node = node.children[ch]
        node.is_end = True

    def is_complete(self, word):
        node = self.root
        for ch in word:
            node = node.children[ch]
            if not node.is_end:
                return False
        return True

    def find_longest_complete(self, words):
        ans = ""
        for word in words:
            if self.is_complete(word):
                if len(word) > len(ans) or (len(word) == len(ans) and word < ans):
                    ans = word
        return ans

words = ["a", "banana", "app", "appl", "ap", "apply", "apple"]
trie = Trie()
for w in words:
    trie.insert(w)

print(trie.find_longest_complete(words))
