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

**Explanation** grep selects only the lines that contain “/login”.
wc -l counts how many such lines there are.


---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![task 2](task2.png)

**Explanation** grep finds all lines that contain “Smith”.
wc -l counts those lines.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

This file does not exsits.

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation** cut selects the column with the age.
sort puts the ages in order.
uniq -c counts how many times each age appears.
The second sort -nr orders the counts from highest to lowest.
head -1 shows the most frequent age.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task 5](task5.png)

**Explanation** cut extracts the first and last name.
sort prepares the names for counting.
uniq -c counts how often each name appears.
sort -nr lists them from most common to least.
head -10 shows the top ten names.

### 6. How many unique users are in app_small.log?

![task 6](task6.png)

**Explanation** cut extracts the field containing the username.
The second cut removes the prefix (for example, “user=”).
sort organizes the usernames.
uniq removes duplicates.
wc -l counts how many unique usernames remain

### 7. Which status code appears most often in access_medium.log? 

![task 7](task7.png)

**Explanation** cut extracts the column with the status code.
sort prepares the values for counting.
uniq -c counts each code.
sort -nr orders the counts from highest to lowest.
head -1 shows the most common status code.

### 8. What is the top 3 most common modules in app_small.log?

![task 8](task8.png)

**Explanation** cut -d' ' -f3 extracts the module name from the third column.
sort puts identical module names together.
uniq -c counts how often each module appears.
sort -nr sorts the counts from highest to lowest.
head -3 shows the three most common modules.

### 9. Which task appears most often in system_small.log?

![task 9](task9.png)

**Explanation** cut -d' ' -f4 extracts the field that contains task=....
cut -d'=' -f2 removes the “task=” part and keeps only the task name.
sort orders the task names.
uniq -c counts how many times each task appears.
sort -nr sorts these counts from highest to lowest.
head -1 shows the task that appears most often.
