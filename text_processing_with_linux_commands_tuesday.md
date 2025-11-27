> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task 0](task1.png)

**Explenation:** The command counts how many times the string “/login” appears in the log. grep filters only the lines containing that path, and wc -l returns the total number of matching entries.

---

### 2. How many different ages are in fullnames_with_age.txt?

![task 0](task2.png)

**Explenation:** To determine the number of unique ages, we extract the age column using cut. Sorting the values groups identical ages together, allowing uniq to remove duplicates. Finally, wc -l counts the remaining distinct ages.

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task 0](task3.png)

**Explenation:** We extract the first-name column with cut, sort the values, remove duplicates using uniq, and count the unique names with wc -l.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 0](task4.png)

**Explanation:** This pipeline identifies which age appears most frequently. We isolate the age column, sort it, and use uniq -c to attach occurrence counts. A numeric sort places the least frequent first, and tail -1 selects the age with the highest count.

---

### 5. Which username failed login most often in auth_small.csv?

![task 0](task5.png)

**Explanation:** The pipeline finds the user with the most failed login attempts. grep -i "FAIL" filters failed entries, cut extracts the username field, and sorting allows uniq -c to count occurrences per user. A final numeric sort and tail -1 return the single most frequent failing user.

---

### 6. How many lines in system_small.log have ok=true?

![task 0](task6.png)

**Explanation:** We filter all log entries containing the string ok=true. The result is piped to wc -l, giving the total number of successful events.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task 0](task7.png)

**Explanation:** Two cut commands isolate the log level value. Sorting groups identical levels, uniq -c counts them, and after a numeric sort, tail -1 returns the most common log level.

---

### 8. What is the top 3 most common actions in app_small.log?

![task 0](task8.png)

**Explanation:** We extract and clean the action field using two cut commands. Sorting the actions prepares them for uniq -c, which produces frequency counts. Sorting in reverse numeric order highlights the most common actions, and head -3 outputs the top three.

---

### 9. How many unique users are in app_small.log?

![task 0](task9.png)

**Explanation:** To count distinct users, we extract the user ID through two cut operations, sort the results, pass them through uniq to eliminate duplicates, and use wc -l to get the number of unique user IDs.

---
