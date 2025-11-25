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

Example:

![task 1](task1.png)

**Explanation** I used the grep command to find lines that have "/login" in them, and then I piped that into wc -l to count the number of lines.

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 2](task2.png)

**Explanation** I used awk to print the last column which is the age. Then I used sort so that uniq could work to remove duplicates, and finally wc -l counted how many unique ages there are.

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 3](task3.png)

**Explanation** First I grabbed the first column using awk. Then I sorted the names and used uniq to make sure I only had one of each name, then counted the total with wc -l.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 4](task4.png)

**Explanation** I got the ages using awk, then used uniq -c to count how many times each age shows up. Then I sorted it by number with -nr to get the biggest one on top and used head -n 1 to see the winner.

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 5](task5.png)

**Explanation** I used grep to find "Fail", then because it is a csv I used cut with a comma delimiter to get the username column. Then I counted them with uniq -c and sorted to see who failed the most.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 6](task6.png)

**Explanation** I just used grep to search for the specific text "ok=true" inside the log file and used wc -l to count how many lines were found.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 7](task7.png)

**Explanation** I used grep with -oE to only output the words INFO, WARN, or ERROR. Then I did the standard sort and uniq -c to count them up, and sort -nr shows the most frequent one first.

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 8](task8.png)

**Explanation** I used awk to get the action column from the file. Then I used uniq -c to count the actions, sorted them in reverse order, and used head -n 3 to just show the top 3 common ones.

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 9](task9.png)

**Explanation** I extracted the user column using awk. I had to sort it first, then used uniq to remove duplicates, and finally wc -l gave me the number of unique users.

---
