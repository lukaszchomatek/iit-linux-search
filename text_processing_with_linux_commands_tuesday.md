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

**Explanation:** ***grep*** - leaves only lines that have /login in them and ***wc -l*** - counts how many of those lines are there

---

### 2. How many different ages are in fullnames_with_age.txt?

![task 2](task2.png)
**Explanation:** first ***cut*** - cuts out everything except age=_  (leaving only text after the second space), second ***cut*** - cuts out the 'age =' leaving only the numbers, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences, ***wc -l*** - counts the lines (so how many different numbers there are)

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task 3](task3.png)

**Explanation:** ***cut*** - cuts out everything except first names, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences, ***wc -l*** - counts the lines (so how many unique names there are)

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation:** first ***cut*** - cuts out everything except age=_, second ***cut*** - cuts out the 'age =' leaving only the numbers, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences (it shows how many there are of a certain number and then displays the number next to it), ***sort -nr*** - sorts them reversed (from biggest to smallest - so from the most often appering to the least), ***head -1*** - shows only the first one (the most often appearing)

---

### 5. Which username failed login most often in auth_small.csv?

![task 5](task5.png)

**Explanation:** ***grep*** - leaves only lines that have FAIL in them, ***cut*** - cuts out everything except username,  ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences (counts how many each user had failed login attempts), ***sort -nr*** - sorts them reversed (from biggest to smallest - so from the most failed logins to the least), ***head -1*** - shows only the first one (the user with the most failed logins and how many were there)

---

### 6. How many lines in system_small.log have ok=true?

![task 6](task6.png)
**Explanation:** ***grep*** - leaves only lines that have ok=true in them and ***wc -l*** - counts how many of those lines are there

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task 7](task7.png)

**Explanation:** the first two ***cut*** - cuts out everything except level, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences, ***sort -nr*** - sorts them reversed (from biggest to smallest - so from the most often appering to the least), ***head -1*** - shows only the first one (the most often appearing and how many times it does)

---

### 8. What is the top 3 most common actions in app_small.log?

![task 8](task8.png)

**Explanation:** the first two ***cut*** - cuts out everything except action, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences, ***sort -nr*** - sorts them reversed (from most common to least), ***head -3*** - shows the top 3

---

### 9. How many unique users are in app_small.log?

![task 9](task9.png)

**Explanation:** the first two ***cut*** - cuts out everything except user, ***sort*** - sorts them as it's required for uniq, ***uniq -c*** - counts unique occurences (and shows them in seperate lines), ***wc -l*** - counts the lines (so how many users there are)

---
