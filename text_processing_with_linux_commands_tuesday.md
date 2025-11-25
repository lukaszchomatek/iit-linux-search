> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---
![Task 1 Result](Task1.png)
Explanation: 'wc' is a command to get the lines, words and characters and flag '-l' let's us count only the lines.

![Task 2 Result](task2.png)
Explanation: awk is a processing tool, $NF refers to last column, '|' passes the output to a pevious command, sort sorts the data preparing it for the uniq command which filters the duplicate lines, wc -l counts the lines found by the previous commands

![Task 3 Result](Task3.png)
Explanation: Basicly the same as in the previous task the diffrence is $1 which referes to only the first column of each line

![Task 4 Result](Task4.png)
Explanation: find extracts the last column form every line, -c flags the number of occurrencies , -n sorts numercially, -r reverses the order putting the most frequent numbers art the top, head -n 1 selects only the first line of output.

![Task 5 Result](Task5.png)
Explanation: grep - "FAIL" searches for lines containing the 'FAIL' phrase $(find...) automaticly findes the file, -F tells awk to treat commas as a seperator between columns '{priny $2}' extracts the data from the second column, sort | uniq -c sorts the names so duplicates are adjacent, then counts how many times each name appears, -nr sorts the counts in the reverse numerical order, head -n 1 show only the top result.

![Task 6 Result](Task6.png)
Explanation: grep "ok=true" command for searching lines with reular expression it filter it to only lines that contain "ok=true" string, wc - l counts the numbers of lines.

![Task 7 Result](Task7.png)
Explanation: $(find . -name "system_small.log") locates the file path automatically, grep -oE "INFO|WARN|ERROR" ... -o tells grep to output only the matching part of the line, -E allows the use of '|' to search for everything declared simultaneously, sort everything togheter, uniq -c counts occurrance of every level, sort -nr sorts the counts numerically, head -n 1 shows only the most frequent level.

![Task 8 Result](Task8.png)
Explanation: cat ./logs/app_small.log this command starts the process by reading the content of the log file, tr -s " ", the output from cat is passed to tr. The tr -s " " command ensures consistency by squeezing multiple consecutive spaces into a single space, sort arranges the values alphabetically, uniq -c counts every time an adjacetn value appears, sort -nr the stream of counted values is sorted again. The -n flag ensures the sort is treated as a number (not text), and the -r flag performs a reverse (descending) sort. This places the highest counts at the very top of the list, head -n 3shows only the top 3 results

![Task 9 Result](task9.png)
Explanation: cat logs/app_small.log reads and accesses the file, tr -s ' ' is explained in the previous step, cut -d ' ' -f4 cut extracts sections from each line -d ' ' tells the command that the fields are separated by a space -f4 tells the command to extract only the 4th column.