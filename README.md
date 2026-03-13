def bubble_sort(arr):
n = len(arr)
print(f"Original List: {arr}\n")

# Outer loop to traverse through all array elements
for i in range(n):
# Flag to optimize: if no elements are swapped, the list is sorted
swapped = False

# Last i elements are already in place
for j in range(0, n - i - 1):
# Compare adjacent elements
if arr[j] > arr[j + 1]:
# Swap if the element found is greater than the next element
arr[j], arr[j + 1] = arr[j + 1], arr[j]
swapped = True

# Output the state of the list after each full pass
print(f"Pass {i + 1}: {arr}")

# If no two elements were swapped by inner loop, then break
if not swapped:
print("\n No swaps occurred. The list is already sorted!")
break

return arr

# --- Execution ---
data = [64, 34, 25, 12, 22, 11, 90]
sorted_data = bubble_sort(data)

print("-" * 30)
print(f"Final Sorted List: {sorted_data}")


Output:
Original List: [64, 34, 25, 12, 22, 11, 90]

Pass 1: [34, 25, 12, 22, 11, 64, 90]
Pass 2: [25, 12, 22, 11, 34, 64, 90]
Pass 3: [12, 22, 11, 25, 34, 64, 90]
Pass 4: [12, 11, 22, 25, 34, 64, 90]
Pass 5: [11, 12, 22, 25, 34, 64, 90]

 No swaps occurred. The list is already sorted!
------------------------------
Final Sorted List: [11, 12, 22, 25, 34, 64, 90]
