import heapq

def tallest_5_system(all_people_heights):
    bus = []
    k = 5

    for height in all_people_heights:
        if len(bus) < k:
            heapq.heappush(bus, height)
            print(f"Entered the bus: {height}cm")
        else:
            if height > bus[0]:
                old_person = heapq.heappushpop(bus, height)
                print(f"New person ({height}cm) replaced the old person ({old_person}cm)")
            else:
                print(f"New person ({height}cm) is too short, no room available")

    return sorted(bus, reverse=True)

heights = [170, 185, 160, 190, 175, 195, 188, 165, 200]
print("--- Starting the Bus System ---")
top_5 = tallest_5_system(heights)

print("\nTop 5 tallest people in the bus:")
print(top_5)
