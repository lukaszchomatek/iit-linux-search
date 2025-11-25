> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** cd to open directory, wc -l counts lines

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task 1](task1.png)

**Explanation** Write the explanation why the specific command was used.

grep searches for patterns like you can with regex, -c counts lines

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![task 2](task2.png)

**Explanation** same as before, it searches for lines but that works since there is no Smith Smith in the filr

### 3. How many occurrences of Smith are in fullnames_simple.txt?



**Explanation** File does not exist :p 

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation** cut gets us all ages in the file (-f 2 is column 2, -d is delimiter). sort first to count occurences (I don't get why we need to sort but the lecture pdf says so :p), sort again so most common age is on top and head is for printing

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task 5](task5.png)

**Explanation** same as before, head -n 10 prints 10 first lines

### 6. How many unique users are in app_small.log?

![task 6](task6.png)

**Explanation** we use two cuts to trim the users, sort, delete duplicates and print =<^.^>=

### 7. Which status code appears most often in access_medium.log? 

![task 7](task7.png)

**Explanation**  get the correct column with cut, finding most common same as always ^^

### 8. What is the top 3 most common modules in app_small.log?

![task 8](task8.png)

**Explanation** Write the explanation why the specific command was used.

### 9. Which task appears most often in system_small.log?
![task 9](task9.png)

**Explanation** again we use two cuts to isolate the data, (get unique counts, sort and print)
