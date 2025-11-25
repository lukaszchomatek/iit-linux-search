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

![task 1](task1.png)

**Explanation** cat is used to print contents of the file. grep for filtering using REGEX and wc -l counts lines

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task 2](task2.png)

**Explanation** one cut is for getting "age=\d\d" and the second is to trim the "age=". sort -u as it is written in the man page _does not detect repeated lines unless they are adjacent. You may want to sort the input first, or use 'sort -u'_. uniq filters trims duplicates. wc -l counts entries.

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task 3](task3.png)

**Explanation** cut is used to get the names. sort -u as it is written in the man page _does not detect repeated lines unless they are adjacent. You may want to sort the input first, or use 'sort -u'_. uniq filters trims duplicates. wc -l counts entries.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task4](task4.png)

**Explanation** cut to get "age=\d\d", cut to get "\d\d", uniq -D to group duplicates, uniq -c to count. sort -u to sort by prefix from uniq -c. tail -n 1 gets the last line and awk to format printing

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task5](task5.png)

**Explanation** grep to get those who failed. cut to get names. sort to allow for counting using uniq -c. sort -u to get the one failed the most. tail to get the last line and awk for formatting and printing

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task6](task6.png)

**Explanation** grep to filter, wc -l to count

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task7](task7.png)

**Explanation** cut to get level. sort to allow uniq -c to count. head to get only the one the most frequent and awk to print the answer

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task8](task8.png)

**Explanation** cut to get "\w msg" and second to transform it into "\w" (our action) sort to allow for counting using uniq -c. sort to get have the most common easily identifiable. tail to get only the last one and awk to print

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

![task9](task9.png)

**Explanation** cut to get "\w action" and second to get username. sort to allow uniq to work and wc -l to count

---
