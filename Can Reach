graph = {
    1: [2, 3],
    2: [1, 4],
    3: [1],
    4: [2, 5],
    5: [4]
}

def can_reach(graph, start, target, visited=None):
    if visited is None:
        visited = set()

    if start == target:
        return True

    visited.add(start)

    for neighbor in graph.get(start, []):
        if neighbor not in visited:
            if can_reach(graph, neighbor, target, visited):
                return True
    
    return False

print(f"Can reach from 1 to 5? {can_reach(graph, 1, 5)}")
print(f"Can reach from 1 to 10? {can_reach(graph, 1, 10)}")
