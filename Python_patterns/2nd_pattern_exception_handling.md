### Pattern: Read Numbers from File with Exception Handling

### Problem

Read numbers from a file and handle invalid data and missing file errors.

### Pattern Code

try:
    with open("numbers.txt","r") as f:
        for line in f:
            line = line.strip()
            try:
                number = int(line)
                print(number)
            except ValueError:
                print("Invalid number:", line)

except FileNotFoundError:
    print("File not found")

### Key Ideas

with → safe file handling

strip() → remove newline characters

int() → convert string to number

ValueError → invalid number in file

FileNotFoundError → missing file

### When to Use

Reading numeric data from files

Data validation

Robust scripts

Log parsing

ETL pipelines
