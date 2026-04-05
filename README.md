# Iterative Binary Search (Python)

This project implements the **Iterative Binary Search algorithm** in Python. Binary search is an efficient searching technique that works on **sorted arrays** with a time complexity of **O(log n)**.

---

## 🚀 Features

- Iterative implementation (no recursion)
- Efficient search in sorted arrays
- Handles "not found" cases
- Simple and beginner-friendly

---

## 📂 Project Structure
├── iterative_binary_search.py
├── README.md
└── requirements.txt


---

## 🧠 Algorithm Explanation

Binary Search works by repeatedly dividing the search space in half:

1. Start with the middle element of the array
2. If the target equals the middle element → return index
3. If target is greater → search right half
4. If target is smaller → search left half
5. Repeat until element is found or range becomes invalid

---

## 🧾 Code Overview

```python
def IBinarySearch(arr, target):
    low = 0
    high = len(arr) - 1

    while low <= high:
        mid = (low + high) // 2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1

    return -1
```
▶️ How to Run
1. Clone the repository
git clone https://github.com/your-username/iterative-binary-search.git
cd iterative-binary-search
2. Run the script
python iterative_binary_search.py
💻 Example
Array: [1, 3, 5, 7, 9]
Enter the target value: 5
Index of 5: 2

If element is not found:

Enter the target value: 6
Index of 6: Not found
⚠️ Important Notes
The array must be sorted before applying binary search
Works only with comparable elements (integers, floats, strings)
⏱️ Complexity
Type	Complexity
Time	O(log n)
Space	O(1)
🛠️ Future Improvements
Add recursive implementation
Support dynamic user input arrays
Add unit tests
Convert into a reusable module
