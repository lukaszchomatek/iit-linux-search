> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

<img width="1094" height="58" alt="image" src="https://github.com/user-attachments/assets/f7495dfe-cf61-493a-9906-83906149234a" />


**Explanation** We use grep to filter lines that contain "/login" and wc -l to count the output lines

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

<img width="1387" height="58" alt="image" src="https://github.com/user-attachments/assets/4a70b5c6-5a8d-4ccb-89fd-d764d273951e" />


**Explanation** cut to select only surnames, grep to filter "Smith" and wc to count lines

### 3. How many occurrences of Smith are in fullnames_simple.txt?

file doesn`t exist

**Explanation** Write the explanation why the specific command was used.

### 4. Which age is most frequent in fullnames_with_age.txt?

<img width="1531" height="57" alt="image" src="https://github.com/user-attachments/assets/cee094e2-2d24-4817-ac05-b6a6aa5d0550" />



**Explanation** cut to separate the age values, sort for uniq func, then uniq -c count unique occurences, sort -nr to sort them descending, so the first is the most frequent
### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

<img width="1491" height="291" alt="image" src="https://github.com/user-attachments/assets/ab684f31-159c-4083-b1ab-b9b78e86584c" />

**Explanation** cut to separate Names and surnames, sort for uniq, uniq -c to count unique, sort to sort them descending, and head to get first 10 results
### 6. How many unique users are in app_small.log?

<img width="1429" height="50" alt="image" src="https://github.com/user-attachments/assets/130adb3f-ee0a-4793-a737-2a30fb3af093" />

**Explanation** 2 cuts to separate the users names, sort for uniq, uniq to display only unique values, wc -l to count the users

### 7. Which status code appears most often in access_medium.log? 

<img width="1319" height="253" alt="image" src="https://github.com/user-attachments/assets/1779a6af-28cb-4cba-b2bd-e38d4f444877" />


**Explanation** cut to get the status code column, sort for uniq, uniq -c to count the uniq occurences, sort -r to sort in descending order, and the first appears the most

### 8. What is the top 3 most common modules in app_small.log?

<img width="1385" height="109" alt="image" src="https://github.com/user-attachments/assets/7ea5a56d-0cb3-48b0-b3bf-46a20f26073b" />


**Explanation** cut to get the module column, sort for uniq, uniq -c  to count the uniq occurences, sort -r to sort in descending order, head -3 to display top 3

### 9. Which task appears most often in system_small.log?

<img width="1613" height="55" alt="image" src="https://github.com/user-attachments/assets/2f6a2f86-49d7-4a60-8ced-dd31a42376ac" />


**Explanation** 2 cuts to separate the task names, sort for uniq, uniq -c  to count the uniq occurences, sort -nr to sort in descending order, head -1 to display top 1
