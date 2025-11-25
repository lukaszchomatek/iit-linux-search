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
![task 1](<task 1.png>)

**Explanation**

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 2](<task 2-1.png>)

**Explanation** 

This pipeline identifies the most frequent age in the dataset. First, we remove the age column, then sort the values. Next, we use uniq -c to count occurrences of each unique age. After that, we apply sort -n to arrange the results by frequency. Finally, tail -1 retrieves the last line, which corresponds to the age with the highest count.


---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 3](<task 3.png>)
**Explanation** Write the explanation why the specific command was used.
This follows the same approach as counting unique ages. We use cut to extract the column containing first names, then sort them to group identical entries. Next, uniq removes duplicates, and wc -l returns the total number of distinct names.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 4](<task 4.png>)

**Explanation** Write the explanation why the specific command was used.
This pipeline determines the most frequent age in the dataset. First, we extract the age column using cut and sort the values. Then, uniq -c adds a count next to each unique age. Next, we apply sort -n to arrange the results by frequency. Finally, tail -1 selects the last line, which represents the age with the highest count.

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 5](<task 5.png>)

**Explanation** Write the explanation why the specific command was used.
We begin by using grep to filter the log and retain only failed events. Next, cut (with a comma as the delimiter) extracts the username from those lines. After that, we sort the usernames, apply uniq -c to count failures per user, and finally use sort -n | tail -1 to identify and display the username with the highest failure count.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 6](<task 6.png>)

**Explanation** Write the explanation why the specific command was used.
This is a simple filter-and-count operation. We use grep to scan the log file for lines containing "ok=true" (indicating successful operations). The results are then piped to wc -l, which returns the total number of successful entries.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 7](<task 7.png>)

**Explanation** Write the explanation why the specific command was used.
We use two cut commands to isolate the log level (e.g., extracting "INFO" from "level=INFO"). Next, we sort the values and apply uniq -c to count occurrences of each level. Finally, sort -n | tail -1 retrieves the log level (INFO, WARN, or ERROR) that appears most frequently.

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 8](<task 8.png>)

**Explanation** Write the explanation why the specific command was used.
This process is similar to finding the single most frequent item, with one key difference. We extract and clean the action column using cut, then sort the values and apply uniq -c to count occurrences. Next, we use sort -n -r to arrange the counts in descending order (the -r flag reverses the sort). Finally, head -3 selects the top three lines, representing the three most common actions.

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task 9](<task 9.png>)


**Explanation** Write the explanation why the specific command was used.
To count unique users, we use two cut commands to extract and clean the user ID from each log line. The output is then sorted and passed through uniq to remove duplicates. Finally, wc -l counts the remaining lines, giving the total number of distinct users.
---