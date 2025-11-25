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

**Explanation** grep was used to search for lines with specific pattern. wc -l to count this specific patterns.

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 2](task2.png)

**Explanation** sort -n arranges numerically. uniq -c counts occurrences. wc -l writes it.

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 3](task3.png)

**Explanation** -d ' ' cuts spaces. -f2 selects the second field. sort arranges the lines. uniq chooses the specific lines. wc -l counts these lines.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 4](task4.png)

**Explanation** awk '{print $NF}' takes the last part of the line, which is age. sort - arranges, uniq -c counts repetatives, sort -nr sorts in nummercal order with increasing order, head -1 shows the most frequent age

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 5](task5.png)

**Explanation** grep was used to search for lines with specific pattern. cut -d', ' to cut out the ', ' sign. -f2 to choose second field. sort to arrange, uniq -c to count specifics and head -1 to choose our option.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 6](task6.png)

**Explanation** grep was used to search for lines with specific pattern. wc -l to count them.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 7](task7.png)

**Explanation** grep -o  outputs only the part of the line that matches the pattern.

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 8](task8.png)

**Explanation** head -3 chooses firtst 3 options.

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 9](task9.png)

**Explanation** Write the explanation why the specific command was used.

---