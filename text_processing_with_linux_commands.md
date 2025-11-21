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

![task 1](task1.png)

grep "/login" "access_small.log" | wc - l 
**Explanation** Write the explanation why the specific command was used.

The specified command "grep" checks which lines have signs "/login". The | sign transmits results from the first command to the second command. The wc command count data in a given file and -l counts it. 

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?
![task 2](task2.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
The specified command "grep" checks which lines have word "Smith". The | sign transmits results from the first command to the second command. The wc command count data in a given file and -l counts it. 

### 3. How many occurrences of Smith are in fullnames_simple.txt?


![task 2](task2.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

The specified command "grep" checks which lines have word "Smith". The | sign transmits results from the first command to the second command. The wc command count data in a given file and -l counts it. 

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task4](task4.png)

**Explanation** Write the explanation why the specific command was used.
cut - remove column -f take one column that I want to stay | sort -sorts results alphabitacelly | uniq -c - takes unique values | sort -nr sorts alphabetically in reverse order| head -n 1  - show  1  first value

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task5](task5.png)

**Explanation** Write the explanation why the specific command was used.
cut - remove column -f take one column that I want to stay -d is for showing what devides collumns | sort -sorts results alphabitacelly | uniq -c - takes unique values | head -n 10 - shows 10 first values
### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task6](task6.png)

**Explanation** Write the explanation why the specific command was used.
cut - remove column -f take one column that I want to stay -d is for showing what devides collumns | sort -sorts results alphabitacelly | uniq -c - takes unique values | wc - l counts occurences of a data
### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
