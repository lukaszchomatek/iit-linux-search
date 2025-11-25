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

![task1](Task1.png)

**Explanation** grep -c is used to count how many lines contain /login

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task2](Task2.png)

**Explanation** grep -o 'age...' extracts only age=xx part, sort sorts them, then uniq gets rid of the duplicates and wc-l counts how many remain

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task3](Task3.png)

**Explanation** cut -d" " -f1 splits each line by space and extracts the first field (so first name), then just sort, uniq to remove duplicated and then wc -l to count.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task4](Task4.png)

**Explanation** First we extract just the ages, then we divide it by = sign, then we take just the number, sort it, use uniq -c to make it count the duplicates then sort by the number and output the highest one (So most common is 56 with 222 occurences)

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task5](Task5.png)

**Explanation** Very similar to task 4. Keep the lines with FAIL, count unique names, list the one with the most occurences.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task6](Task6.png)

**Explanation** grep -c counts how many lines contain a phrase, same as Task1

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task7](Task7.png)

**Explanation** grep -o extracts just the fragment, then we only leave the 2nd field (INFO,WARN or ERROR), then sort them, use uniq -c to count uniques, sort by number of occurences, then output the highest one

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task8](Task8.png)

**Explanation** grep -o extracts just the fragment, then we only leave the 2nd field (the action), then sort them, use uniq -c to count uniques, sort by number of occurences, output the 3 highest ones

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task9](Task9.png)

**Explanation** grep -o extracts just the fragment, then we only leave the 2nd field (the user), then sort them, use uniq remove duplicates, then use wc -l to count how many are remaining (so unique ones)

---

---
