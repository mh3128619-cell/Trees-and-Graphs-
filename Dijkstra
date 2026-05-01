import heapq

def dijkstra(graph, start):
    distances = {node: float('inf') for node in graph}
    distances[start] = 0
    
    priority_queue = [(0, start)]
    
    while priority_queue:
        current_distance, current_node = heapq.heappop(priority_queue)
        
        if current_distance > distances[current_node]:
            continue
            
        for neighbor, weight in graph[current_node].items():
            distance = current_distance + weight
            
            if distance < distances[neighbor]:
                distances[neighbor] = distance
                heapq.heappush(priority_queue, (distance, neighbor))
                
    return distances

cairo_map = {
    'Haram': {'Mohandessin': 10, 'Downtown': 5},
    'Downtown': {'Mohandessin': 2, 'Maadi': 8},
    'Mohandessin': {'Maadi': 3},
    'Maadi': {}
}

shortest_paths = dijkstra(cairo_map, 'Haram')
print(f"Shortest times from Haram to all areas: {shortest_paths}")
