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


---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 2](task2.png)
**Explanation** Write the explanation why the specific command was used.
To count the unique ages, we first use cut to extract only the column with the age data. We must use sort to group identical ages together, which allows uniq to remove all duplicates.Then we use wc -l to count how many unique ages are left.
---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 3](task3.png)
**Explanation** Write the explanation why the specific command was used.
We use cut to grab the column with first names. We sort them to group identical names, then use uniq to eliminate duplicates. wc -l gives us the final count of names.
---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 4](task4.png)
**Explanation** Write the explanation why the specific command was used.
This pipeline finds the biggest number. We cut out the age column, sort it, and use uniq -c to add a count next to each unique age. We then use a second sort -n to order the results by that new number column. tail -1 grabs the last line, which is the age with the largest count.
---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 5](task5.png)
**Explanation** Write the explanation why the specific command was used.
This pipeline is used to find the most frequent failing user. We start with grep -i "FAIL" to filter the log for all failed login attempts, ignoring letter case. We then use cut -d',' -f2 to extract the correct field containing the username from the comma-separated data. The resulting usernames are sorted, counted by uniq -c to calculate the failure frequency for each user. Then, sort -n | tail -1 extracts the single username with the highest failure count, which is dave with 181 failures.
---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 6](task6.png)
**Explanation** Write the explanation why the specific command was used.
We use grep to filter the entire log file, looking specifically for "ok=true". The pipe sends these filtered lines to wc -l to get a final tally of how many successful lines there were.
---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 7](task7.png)
**Explanation** Write the explanation why the specific command was used.
We use two cut commands to extract the log level. We then sort and use uniq -c to count how many times each level appears. Finally, we sort -n | tail -1 to grab the one log level that occurred the most often.
---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 8](task8.png)
**Explanation** Write the explanation why the specific command was used.
We cut and clean the action column, sort, and use uniq -c to get the counts. The second sort -n -r sorts the counts from highest to lowest. Finally, head -3 grabs the top three lines, which are the three most common actions.
---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 9](task9.png)
**Explanation** Write the explanation why the specific command was used.
To count unique users, we use two cut commands to successfully extract and clean the user ID from the log lines. The data is then "sort" and passed to uniq to ensure only one instance of each user ID remains. The final wc -l command counts the remaining lines to give us the total number of distinct users.
---