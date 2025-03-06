# Overview

This script demonstrates a simple process of splitting a set of numeric IDs into two lists, sorting them, and then performing two main calculations:

1. **Total Distance**  
   - For each index `i`, compute the absolute difference between the corresponding elements in the sorted left and right lists.  
   - Sum these differences to get the total distance.

2. **Total Similarities**  
   - **Optimized Approach**: Instead of calling `.count()` repeatedly, this script uses a dictionary to track how many times each ID appears in the right list.  
   - For each unique number in the sorted left list, we look up its frequency in the dictionary, multiply the number by its frequency, and add that to the running total of similarities.

---

## Steps in Detail

1. **Populate Left & Right Lists**  
   - Read the multiline string of numeric IDs.  
   - Split them and assign alternating items to `left_list` and `right_list`.

2. **Sort the Lists**  
   - Sort each list independently from smallest to largest.

3. **Calculate Total Distance**  
   - Compare each pair of indices (`i`) in the sorted left and right lists.  
   - Use `abs(int(sorted_left_list[i]) - int(sorted_right_list[i]))` to find the distance. Use abs() to get the result as a positive number.
   - Accumulate the result into `total_distance`.

4. **Calculate Total Similarities**  
   - Build a dictionary (hash map) of each ID’s frequency in the right list.  
   - For each ID in the left list, multiply the ID by its frequency from the dictionary, then add to `total_similarities`.  
   - This approach avoids scanning the right list for each element, significantly reducing complexity.

---

## Usage

1. Clone or download this repository.
2. Run the script with Python (3.x or higher recommended):

```bash
python solution-v2.py
```

## Output

1. The count of IDs in each list.
2. The total distance between sorted left and right IDs.
3. The total similarities, based on repeated occurrences.