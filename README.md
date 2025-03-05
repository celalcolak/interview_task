# Overview

This script demonstrates a simple process of splitting a set of numeric IDs into two lists, sorting them, and then performing two main calculations:

1. **Total Distance**  
   - For each index `i`, compute the absolute difference between the corresponding elements in the sorted left and right lists.  
   - Sum these differences to get the total distance.

2. **Total Similarities**  
   - For each unique number in the sorted left list, count how many times it appears in the sorted right list.  
   - Multiply that number by its frequency and add it to the running total of similarities.

---

## Steps in Detail

1. **Populate Left & Right Lists**  
   - Read the multiline string of numeric IDs.  
   - Split them and assign alternating items to `left_list` and `right_list`.

2. **Sort the Lists**  
   - Sort each list independently from smallest to largest.

3. **Calculate Total Distance**  
   - Compare each pair of indices (`i`) in the sorted left and right lists.  
   - Use `abs(int(sorted_left_list[i]) - int(sorted_right_list[i]))` to find the distance.  
   - Accumulate the result into `total_distance`.

4. **Calculate Total Similarities**  
   - For each unique ID in the sorted left list, determine how many times it appears in the sorted right list.  
   - Multiply the ID by the count of occurrences and add to `total_similarities`.

---

## Usage

1. Clone or download this repository.
2. Run the script with Python (3.x or higher recommended):

```bash

python script_name.py
```

## The script prints out:
1. The count of IDs in each list.
2. The total distance between sorted left and right IDs.
3. The total similarities based on repeated occurrences.
