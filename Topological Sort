def topological_sort(tasks):
    visited = set()
    stack = [] 

    def dfs(course):
        visited.add(course)

        for neighbor in tasks.get(course, []):
            if neighbor not in visited:
                dfs(neighbor)
        
        stack.append(course)

    for course in tasks:
        if course not in visited:
            dfs(course)

    return stack[::-1]

tasks = {
    "Programming 1": ["Data Structures"],
    "Data Structures": ["Algorithms"],
    "Algorithms": [],
    "Mathematics": []
}

order = topological_sort(tasks)
print(f"The logical order of courses: {order}")
