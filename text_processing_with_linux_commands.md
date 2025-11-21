> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![alt text](<Screenshot 2025-11-21 at 11.27.22.png>)

**Explanation**
Grep searches for text in the file. The -c option returns the number of occurrences, and the string /login indicates that only lines containing this path are counted.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![alt text](<Screenshot 2025-11-21 at 11.29.37.png>)

**Explanation** 
Grep -o prints each match on a separate line, and wc -l counts the lines. This gives us a count of all occurrences of the word Smith.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

There is no such file

**Explanation** Write the explanation why the specific command was used.

### 4. Which age is most frequent in fullnames_with_age.txt?

![alt text](<Screenshot 2025-11-21 at 11.43.55.png>)

**Explanation** • cut -d',' -f2 — extracts the second column (age), assuming the data is comma-separated.
• sort — sorts ages to uniq count them.
• uniq -c — counts repeated values.
• sort -nr — sorts descending by occurrence.
• head -1 — selects the most common age.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![alt text](<Screenshot 2025-11-21 at 11.45.23.png>)

**Explanation** Similarly to the previous task, but this time we extract the first and last name column (-f1). head -10 shows the 10 most frequently occurring names.

### 6. How many unique users are in app_small.log?

![alt text](<Screenshot 2025-11-21 at 13.05.29.png>)

**Explanation** • cut -d '=' -f 2 app_small.log | cut -d ' ' -f 1 | sort | uniq -c | wc -l

### 7. Which status code appears most often in access_medium.log? 

![alt text](<Screenshot 2025-11-21 at 12.37.32.png>)

**Explanation**  •	cut extracts specific fields (columns) from each line.
	•	-d ' ' → uses a space as the delimiter between columns.
	•	-f 5 → selects the 5th column from each line of access_medium.log.

### 8. What is the top 3 most common modules in app_small.log?

![alt text](<Screenshot 2025-11-21 at 12.24.43.png>)

**Explanation** • awk '{print $3}' — extracts the module name from the log (assuming it's in column 3).
• sort | uniq -c | sort -nr | head -3 — counts the most common modules and selects the 3 most popular.

### 9. Which task appears most often in system_small.log?

![alt text](<Screenshot 2025-11-21 at 12.26.01.png>)

**Explanation** • awk '{print $2}' — extracts the task name (assuming it's in the 2nd column). • sort | uniq -c | sort -nr | head -1 — counts, sorts, and shows the most common task.
