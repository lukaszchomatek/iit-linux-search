> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task_1](task1.png)

**Explanation:** I used the wc for the count function, and the -l flag to count lines, I found access_small.log is in the log directory, so the path is __logs/access_small.log__ 

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![task_2](task2.png)

**Explanation:** I used grep -i to make it case insensitive just in case of a typo, pipe symbol to put the output of the command and making it input to the wc -l, which counts the occurences.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

![task_3](task2.png)

**Explanation:**

### 4. Which age is most frequent in fullnames_with_age.txt?

![task_4](task4.png)

**Explanation:** I used cut with -d flag for the space delimiter as the fields are separated with a space, , I don't prefix it with names/ because I'm already in the subdirectory. Number 3 after -f flag is for column number 3, which where the name column is. <br />
<br />
Pipe that command with another cut command for it to show me just the numbers and remove the "age=". The delimiter is "=" for this cut command, and the age number belongs to the second column. <br />
<br />Sort it numerically with "sort -n", and then unique count it, with "uniq -c" and sort it from highest to lowest with the -r flag from sort.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task_5](task5.png)

**Explanation:** I used cut command to cut the output to just their first name and las name, i used sort to sort the data. Then I used uniq -c to uniquelly count the occurences of each. Sort it in reverse order from the occurences. And filter it out with the top 10 common occurrences with the "head -n 10" command.

### 6. How many unique users are in app_small.log?

![task_6](task6.png)

**Explanation:** I used the cut command to cut the output on the terminal, and cut the output to just the actual user's name, removing "user=", I used sort to sort the data alphabetically, and then uniq to filter out duplicates, finally using wc -l to count the amount of distinct users in app_small.log

### 7. Which status code appears most often in access_medium.log? 

![task_7](task7.png)

**Explanation:** cut to limit the output to just column number 5, sort the limited output numerically, unique count the occurence, and then sort it in reverse, so highest occurence occurs first. And I used head -n 1 to showcase the most often occured status code.

### 8. What is the top 3 most common modules in app_small.log?

![task_8](task8.png)

**Explanation:** tr with the -s flag is used to convert the convert the double space into a single space in the file, and using the cut cuts the output to my intended seeing. Then I sort the file, and then find the unique values, and reverse sort it, run head -n 3 to see the 3 most common modules.

### 9. Which task appears most often in system_small.log?

![task_9](task9.png)

**Explanation:** I used cut to limit the output to just what I want. Pipe this cut output as the input of another cut command. And then sort it alphabetically, count the unique values with "uniq -c", sort it in reverse order from highest first. Then I use "head -n 1" to find the most often appeared task.
