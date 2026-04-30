class MinHeap:
    def __init__(self):
        self.heap = []

    def insert(self, val):

        self.heap.append(val)

        self._bubble_up(len(self.heap) - 1)

    def _bubble_up(self, index):
        parent_index = (index - 1) // 2

        if index > 0 and self.heap[index] < self.heap[parent_index]:
            self.heap[index], self.heap[parent_index] = self.heap[parent_index], self.heap[index]
            self._bubble_up(parent_index)

    def display(self):
        print("Min-Heap Array:", self.heap)

my_heap = MinHeap()
numbers = [12, 7, 1, 3, 10]

for n in numbers:
    my_heap.insert(n)

my_heap.display()
