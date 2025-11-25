> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task 1](task1.png)

**Explanation** grep command is to filter similiar data. wc command is to count data in a given file. -l parameter is for counting lines.

---

### 2. How many different ages are in fullnames_with_age.txt?

![task 2](task2.png)

**Explanation** sort and -n is to numerically arrange lines. uniq -c is to count occurances. wc command is to count data in a given file. -l parameter is for counting lines.

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task 3](task3.png)

**Explanation** cut is used to split the space and print first column (the names), sort arranges the names and uniq delete the ones that come up multiple time, wc command is to count data in a given file. -l parameter is for counting lines.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation** grep -o extracts the "age=", cut takes the column with ages, then sorts it counts how many times each ages appears, then sorts that so that the most frequent is at the top, then shows it

---

### 5. Which username failed login most often in auth_small.csv?

![task 5](task5.png)

**Explanation** grep "FAIL" extracts the fail lines cut takes the colum with names and FAIL then sorts it counts how many times each FAIL appears, then sorts that so that the most frequent is at the top, then shows it.

---

### 6. How many lines in system_small.log have ok=true?

![task 6](task6.png)

**Explanation** grep command is to filter similiar data. wc command is to count data in a given file. -l parameter is for counting lines.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task7](task7.png)

**Explanation** cut extracts the level=... column, then sorts it, counts how many appear, then sorts it so the most is at the top and prints the first one.

---

### 8. What is the top 3 most common actions in app_small.log?

![task8](task8.png)

**Explanation** grep filters the action=... column then cuts the action column, counts how many appear, then sorts it so the most is at the top and prints the first three.

---

### 9. How many unique users are in app_small.log?

![task9](task9.png)

**Explanation** cut is used to split the space and print users column, sort arranges the unique users and shows them.

---