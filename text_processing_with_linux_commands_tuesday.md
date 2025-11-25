> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

 

Example:

![task 0](task0.png)

**Explanation**  

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task 1](task1.png)

**Explanation**  
grep "/login" filters lines containing /login. wc -l counts these filtered lines to give the total number of login accesses.

---

### 2. How many different ages are in fullnames_with_age.txt?

![task 2](task2.png)

**Explanation**  
grep "/login" filters lines containing /login. wc -l counts these filtered lines to give the total number of login accesses.

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task 3](task3.png)

**Explanation**  
grep "/login" filters lines containing /login. wc -l counts these filtered lines to give the total number of login accesses.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation**  
grep "/login" filters lines containing /login. wc -l counts these filtered lines to give the total number of login accesses.

---

### 5. Which username failed login most often in auth_small.csv?

![task 5](task5.png)

**Explanation**  
grep "/login" filters lines containing /login. wc -l counts these filtered lines to give the total number of login accesses.

---

### 6. How many lines in system_small.log have ok=true?

![task 6](task6.png)

**Explanation**  
grep "ok=true" selects all lines with ok=true. wc -l counts the number of such lines.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task 7](task7.png)

**Explanation**  
awk '{print $3}' extracts the level column. uniq -c counts occurrences, sort -nr sorts descending, and head -1 shows the most frequent level.

---

### 8. What is the top 3 most common actions in app_small.log?

![task 8](task8.png)

**Explanation**  
grep -o "action=[^ ]*" extracts the action= field. cut -d'=' -f2 keeps only the value, uniq -c | sort -nr | head -3 counts and lists the top 3 actions.

---

### 9. How many unique users are in app_small.log?

![task 9](task9.png)

**Explanation**  
grep -o "user=[^ ]*" extracts the user field. cut -d'=' -f2 keeps the username. uniq | wc -l counts unique users.

---