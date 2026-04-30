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

    def search_with_one_mistake(self, word):
        return self._dfs(self.root, word, 1)

    def _dfs(self, node, remaining_word, mistakes_left):
        if not remaining_word:
            return node.is_end_of_word

        char = remaining_word[0]
        next_part = remaining_word[1:]

        if char in node.children:
            if self._dfs(node.children[char], next_part, mistakes_left):
                return True

        if mistakes_left > 0:
            for child_char in node.children:
                if child_char != char:
                    if self._dfs(node.children[child_char], next_part, 0):
                        return True
        
        return False

trie = Trie()
trie.insert("apple")
print(f"Search for 'apple' (correct): {trie.search_with_one_mistake('apple')}")
print(f"Search for 'appze' (one mistake): {trie.search_with_one_mistake('appze')}")
print(f"Search for 'axxle' (two mistakes): {trie.search_with_one_mistake('axxle')}")
