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

**Explanation** Write the explanation why the specific command was used.

grep "/login" finds specific text string "/login" inside a file

| (passes the output of the search to the next command.

wc -l counts the number of lines
---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 2](task2.png)

**Explanation** Write the explanation why the specific command was used.
awk '{print $NF}' prints only the last column of every line, $NF means "Number of Fields" 

sort sorts the data.

uniq leaves only unique entries

wc -l counts the remaining unique lines
---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 3](task3.png)
**Explanation** Write the explanation why the specific command was used.
awk '{print $1}' prints the first column of the file

sort sorts the data

uniq leaves only unique entries

wc -l counts the remaining unique lines
---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 4](task4.png)
**Explanation** Write the explanation why the specific command was used.
awk '{print $NF}' prints only the last column of every line, $NF means "Number of Fields" 

sort -nr sorts the results numerically (-n) and in reverse order (-r), so the highest count is on top.

uniq -c counts unique entries

head -n 1 shows only the top line

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 5](task5.png)
**Explanation** Write the explanation why the specific command was used.

---
grep "fail" filters the file to show only lines containing a failure.

awk -F',' '{print $2}' uses a comma (-F',') as the separator and prints the second column

sort -nr sorts the results numerically (-n) and in reverse order (-r), so the highest count is on top.

uniq -c counts unique entries

head -n 1 shows only the top line
### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 6](task6.png)
**Explanation** Write the explanation why the specific command was used.
grep "ok=true" searches for lines matching that specific pattern.

wc -l counts the number of matching lines
---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 7](task7.png)
**Explanation** Write the explanation why the specific command was used.
grep -oE "INFO|WARN|ERROR" the -o prints only the matching word, the -E allows searching for multiple patterns

sort -nr sorts the results numerically (-n) and in reverse order (-r), so the highest count is on top.

uniq -c counts unique entries

head -n 1 shows only the top line
---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 8](task8.png) 
**Explanation** Write the explanation why the specific command was used.
awk '{print $4}' extracts the fourth column

sort | uniq -c sorts and counts unique 

sort -nr sorts numerically in reverse order.

head -n 3 shows the top 3 results
---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 9](task9.png)
**Explanation** Write the explanation why the specific command was used.
awk '{print $4}': Extracts the fourth column 

sort | uniq sorts unique 

wc -l counts the total number of unique users.
---