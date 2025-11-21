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
![task1](image.png)

**Explanation** grep for searching the matching text and -c counts the number of lines.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task2](image-1.png)

**Explanation** same as for task 1

### 3. How many occurrences of Smith are in fullnames_simple.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task3](image-1.png)

**Explanation** t

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task4](image-2.png)

**Explanation** awk -F', ' ' extracts the age, sort sorts the ages so duplicates are together uniq -c counts how many times each age occurs head -1 keeps only the most frequent age awk '{print $2}'  prints only the age itself (without the count)

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task5](image-3.png)

**Explanation** cut -d',' -f1  extracts everything before the comma (the full name).
sort  sorts names so duplicates are consecutive.
uniq -c  counts how many times each name appears.
sort -nr  sorts by count, descending.
head -10  keeps the 10 most frequent names.

### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task6](image-6.png)

**Explanation** awk '{print $1}'  extracts the first field (username).
sort  sorts usernames so duplicates are consecutive.
uniq  removes duplicates.
wc -l  counts the number of unique users.

### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task7](image-5.png)

**Explanation** awk '{print $5}'  extracts the status code.
sort  sorts the codes.
uniq -c  counts occurrences.
sort -nr  sorts by count, descending.
head -1  keeps the most frequent.
awk '{print $2}' prints just the status code.

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task8](image-7.png)

**Explanation** awk '{print $3}'  extracts the module (third field).
sort  sorts them so duplicates are together.
uniq -c  counts occurrences of each module.
sort -nr  sorts counts descending.
head -3  keeps the top 3 most common modules.

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![task9](image-8.png)

**Explanation** awk -F'task=' '{print $2}' → splits each line at task= and prints what comes after.



awk '{print $1}'  takes only the first word, which is the task name (email).
sort | uniq -c  counts occurrences of each task.
sort -nr  sorts counts descending.
head -1  keeps the most frequent task.
awk '{print $2}'  prints only the task name
