# Radix Sort - Interactive Visualization

## Project Overview

This project is an interactive web application that implements and visualizes Radix Sort Algorithm, developed as part of the Algorithms and Programming II course at Fırat University, Software Engineering Department.

## Algorithm Description


### Problem Definition

Radix Sort solves the problem of sorting a list of integers or strings efficiently without directly comparing the elements. It orders the elements based on their individual digits or characters, handling variable-length inputs and large datasets effectively.

### Mathematical Background

[Explain any mathematical concepts, formulas, or notation relevant to understanding the algorithm]

### Algorithm Steps

1. ***Find the maximum length***: Determine the number of digits (for integers) or characters (for strings) to process.
2. ***Pad strings if necessary***: For strings, pad shorter ones with spaces to equalize length.
3. ***Process each digit/character from least significant to most significant***:

   • Group elements into buckets based on the current digit or character.

   • Collect elements from buckets back into a list while preserving order.
4. ***Repeat*** until all digit/character positions are processed.
5. ***Remove padding*** from strings (if applied) to restore original data.

### Pseudocode

```
RadixSort(arr):
    max_len = length of longest element in arr

    for position from max_len - 1 down to 0:
        buckets = array of empty lists indexed by digit/character value

        for element in arr:
            key = digit or character at position in element (pad if necessary)
            buckets[key].append(element)

        arr = concatenate all buckets in order

    if arr contains padded strings:
        remove padding from elements

    return arr

```

## Complexity Analysis

### Time Complexity

• **Best Case:** O(nk) - The algorithm always processes every digit or character of every element, so even the best case requires scanning all n elements over k digits or characters.
• **Average Case:** O(nk) - Radix Sort consistently performs passes over all digits or characters, making average complexity linear relative to input size and digit length.
• **Worst Case:** O(nk) - Similarly, the worst case requires sorting on all digits/characters without shortcuts.

### Space Complexity

• O(nk) - Extra space is needed for the buckets that temporarily hold elements during each pass, plus space for padding in strings if applicable, where n is the number of elements and k is the number of digits or max string length.



## Features

• Interactive visualization of Radix Sort for both integers and strings
• Step-by-step display of sorting passes with bucket contents
• Supports variable-length strings with automatic padding
• User input validation with clear error messages
• Clear display of sorted output after each sorting step

## Screenshots

![Main Interface](docs/screenshots/main_interface.png)
*Caption describing the main interface*

![Algorithm in Action](docs/screenshots/algorithm_demo.png)
*Caption describing the algorithm in action*

## Installation

### Prerequisites

- Python 3.8 or higher
- Git

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repository.git
   cd your-repository
   ```

2. Create a virtual environment:
   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   streamlit run app.py
   ```

## Usage Guide

1. [Step 1 of using the application]
2. [Step 2 of using the application]
3. [Step 3 of using the application]
...

### Example Inputs

- [Example 1 with expected output]
- [Example 2 with expected output]
- [Example 3 with expected output]

## Implementation Details

### Key Components

- `algorithm.py`: Contains the core algorithm implementation
- `app.py`: Main Streamlit application
- `utils.py`: Helper functions for data processing
- `visualizer.py`: Functions for visualization

### Code Highlights

```python
# Include a few key code snippets that demonstrate the most important parts of your implementation
def key_function(parameter):
    """
    Docstring explaining what this function does
    """
    # Implementation with comments explaining the logic
    result = process(parameter)
    return result
```

## Testing

This project includes a test suite to verify the correctness of the algorithm implementation:

```bash
python -m unittest test_algorithm.py
```

### Test Cases

- [Test case 1 description]
- [Test case 2 description]
- [Test case 3 description]

## Live Demo

A live demo of this application is available at: [Insert Streamlit Cloud URL here]

## Limitations and Future Improvements

### Current Limitations

- [Limitation 1]
- [Limitation 2]
- [Limitation 3]

### Planned Improvements

- [Improvement 1]
- [Improvement 2]
- [Improvement 3]

## References and Resources

### Academic References

1. [Reference 1]
2. [Reference 2]
3. [Reference 3]

### Online Resources

- [Resource 1]
- [Resource 2]
- [Resource 3]

## Author

- **Name:** Saed Abdul Rahim
- **Student ID:** 230543606
- **GitHub:** SaedAbdulRahim

## Acknowledgements

I would like to thank Assoc. Prof. Ferhat UÇAR for guidance throughout this project, and [any other acknowledgements].

---

*This project was developed as part of the Algorithms and Programming II course at Fırat University, Technology Faculty, Software Engineering Department.*
