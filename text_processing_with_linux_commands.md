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

**Explanation** 
- grep searches for lines that contain /login.
- wc command is to count data in a given file. 
- -1 parameter is for counting lines.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 2](task2.png)

**Explanation** 
- grep searches for lines that contain the word “Smith”.
- wc command is to count data in a given file. 
- -1 parameter is for counting lines.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 3](task3.png)

**Explanation** 
- grep searches for lines that contain the word “Smith”.
- wc command is to count data in a given file. 
- -1 parameter is for counting lines.

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 4](task4.png)

**Explanation** 
- cut takes the column that has the age.
- sort puts all ages in order.
- uniq -c counts how many times each age appears.
- sort -nr sorts the counts from biggest to smallest.
- head -1 shows the most common age.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 5](task5.png)

**Explanation** 
- cut takes the first name and last name.
- sort arranges the names alphabetically.
- uniq -c counts how many times each name appears.
- sort -nr sorts the results from most to least common.
- head -10 shows the top ten names.

### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 6](task6n.png)

**Explanation** 
- cut takes the field that has user=....
- The second cut removes user= and keeps only the user ID.
- sort sorts all user IDs.
- uniq removes duplicates so only unique IDs remain.
- wc -l counts how many unique users there are.

### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 7](task7.png)

**Explanation** 
- cut takes the status code column from the log.
- sort arranges the status codes.
- uniq -c counts the number of times each code appears.
- sort -nr sorts them from most frequent to least frequent.
- head -1 shows the most common status code.

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 8](task8.png)

**Explanation** 
- cut extracts the field that contains module=....
- The second cut removes the text before = and leaves only the module name.
- sort sorts all module names.
- uniq -c counts how many times each module appears.
- sort -nr sorts these counts from biggest to smallest.
- head -3 shows the top three modules.

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 9](task9.png)

**Explanation** 
- cut extracts the field that contains task=....
- The second cut removes the task= part.
- sort arranges all task names.
- uniq -c counts how many times each task appears.
- sort -nr sorts the results from the most common task to the least.
- head -1 shows the most frequent task.
