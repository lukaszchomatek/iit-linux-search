> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task 1](1.png)

**Explanation** Write the explanation why the specific command was used.


Grep filters the file for lines with /login. The | passes these results to wc -l, which counts the line total

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![task 2](2.png)

**Explanation** Write the explanation why the specific command was used.

Grep finds all lines containing "Smith". The | passes these results to wc -l to count the lines.
### 3. How many occurrences of Smith are in fullnames_simple.txt?

File does not exist.

**Explanation** Write the explanation why the specific command was used.
File does not exist.

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](4.png)

**Explanation** Write the explanation why the specific command was used.

Cut extracts the age field. The data is sort sort -nr), and head -1 shows the result.
### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task 5](5.png)

**Explanation** Write the explanation why the specific command was used.

cut isolates the names, which are sortsort -nr), and head -10 displays the top ten
### 6. How many unique users are in app_small.log?

![task 6n](6n.png)

**Explanation** Write the explanation why the specific command was used.

cut commands extract and clean the User ID. The IDs are sorted, and uniq removes duplicates. Finally, wc -l displays the result.
### 7. Which status code appears most often in access_medium.log? 

![task 7n](7n.png)

**Explanation** Write the explanation why the specific command was used.

Cut isolates the status code, sort sorts the list than Uniq -c: counts duplicate status codes after that sort -nr: which sorts the counts numerically (-n) in reverse (-r) order to put the highest frequency first, and head -1 shows the result.

### 8. What is the top 3 most common modules in app_small.log?

![task 8n](8n.png)

**Explanation** Write the explanation why the specific command was used.

cut commands, extract and clean the module name. The names are sortuniq -c). The results are sorted, and head -3 shows the top three
### 9. Which task appears most often in system_small.log?

![task 9n](9n.png)

**Explanation** Write the explanation why the specific command was used.

cut commands extract the task name. The results are sorted, and head -1 shows the result.
