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

**Explanation** 

The grep command searches for specific text inside a file.
The -c option counts how many lines contain the given pattern.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![task 2](task2.png)

**Explanation**

grep -o prints each occurrence of the search term on a separate line.
Then wc -l counts those lines.
This combination gives the total number of times “Smith” appears in fullnames_with_age.txt, not just how many lines contain it.

---

### 3. How many occurrences of Smith are in fullnames_simple.txt?

![task 3](task3.png)

**Explanation**

Same logic as in Task 2.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation**

awk '{print $NF}' prints the last field (which is the age), sort sorts all ages, uniq -c counts how many times each age appears,
sort -nr sorts the counts from highest to lowest, head -1 shows the most common age

---

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task 5](task5.png)

**Explanation** 

awk removes the last field (the age), sed 's/ *$//' removes trailing spaces, sort sorts the names alphabetically,
uniq -c counts each unique name, sort -nr sorts by frequency in descending order, head -10 prints the top 10 most common names

---

### 6. How many unique users are in app_small.log?

![task 6](task6.png)

**Explanation** 

grep -o extracts only parts matching user=..., sort prepares them for counting,
uniq removes duplicates, wc -l counts how many unique usernames remain.

---

### 7. Which status code appears most often in access_medium.log? 

![task 7](task7.png)

**Explanation** 

awk '{print $NF}' prints the last field (status code), sort orders them, uniq -c counts how many times each unique status code appears,
sort -nr sorts by count (most frequent first), head -1 shows the most common code

---

### 8. What is the top 3 most common modules in app_small.log?

![task 8](task8.png)

**Explanation**

awk '{print $3}' — gets the 3rd field (HTTP method), sort — sorts the values, uniq -c — counts each unique method,
sort -nr — sorts by frequency (most first), head -3 — shows the top 3 most common methods

---

### 9. Which task appears most often in system_small.log?

![task 9](task9.png)

**Explanation** 

grep -o "task=..." extracts each task, sort prepares values for counting, uniq -c counts unique tasks,
sort -nr sorts by frequency, head -1 shows the task that appears most often
