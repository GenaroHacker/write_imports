
![diag](https://github.com/GenaroHacker/write_imports/assets/95663273/f2d52ee6-474e-47a2-b7f9-f77f0e599115)



# write_imports Utility

This utility is designed to automate the generation of import statements for Python modules in a directory. It has two main parts: a Python script and a Jupyter notebook.

## 

This script contains the core functionality. Here's an overview:

- **Imports**: 
    - `os`: For directory and file operations.
    - `ast`: For abstract syntax tree manipulations to extract class and function names.

### Functions

1. `_extract_items(file_path)`
    - Purpose: Extract function and class names from a Python file.
    - Args: 
        - `file_path`: Path to the Python file.

2. `write_imports(excluded_directories=[])`
    - Purpose: Generate import statements from Python files in the current directory. 
    - Args:
        - `excluded_directories`: Directories to be excluded from the search.
    - Note: By default, '.config' and 'sample_data' directories are excluded.

## 

This Jupyter notebook utilizes the functionality provided by `write_imports.py`.

### Cells

1. **Set Up**
    - Clones the git repository and imports the `write_imports` function.

```
%%capture
#@title Set Up
!git clone https://github.com/GenaroHacker/write_imports.git
from write_imports.write_imports import write_imports
```

2. **Import Statements**
    - Demonstrates how to use the `write_imports` function and displays the generated import statements.

```
%%capture
#@title Import Statements
#Modules: ['write_imports']

print(write_imports([]))

from write_imports.write_imports import write_imports
```

## Usage

To utilize this utility, clone the git repository, run the Python script to ensure all functions are available, and then execute the Jupyter notebook cells to see the automated import statements in action.

---

This README is an overview of the utility's functionality. For in-depth details, refer to the source code.

