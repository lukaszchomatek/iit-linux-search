> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![alt text](image.png)
First part finds the lines with /login in the correct file. Second part counts lines

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![alt text](image-1.png)

**Explanation** First Part searches for "Smith" In the file. 
Second Part uses word count to count lines

### 3. How many occurrences of Smith are in fullnames_simple.txt?

![alt text](image-1.png)
No file

### 4. Which age is most frequent in fullnames_with_age.txt?
![alt text](image-8.png)
1 First command cuts the third field where age is
Second command sorts them
Third command counts unique occurances
Fourth command sorts it from highest to lowest
Fifth command lists only the top 1

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![alt text](image-3.png)
**Explanation** First command cuts first 2 words from the file. 
Second command sorts the names
Third command counts it
Fourth command sorts it from highest to lowest number of occurances
Last command lists 10 results with most occurances

### 6. How many unique users are in app_small.log?
![alt text](image-5.png)

**Explanation** First command cuts the fourth field, user id. 
Second command sorts it
Third command command merges multiple appearences of the same id
Last command counts them.

### 7. Which status code appears most often in access_medium.log? 

![alt text](image-4.png)

**Explanation** First part takes the fifth field. 
Second part sorts them
Third part counts unique occurances
Fourth command sorts them from highest to lowest
Last command lists the first one from top of the list

### 8. What is the top 3 most common modules in app_small.log?

![alt text](image-6.png)

**Explanation** Basically the same as the previous, but lists the top 3 instead of top 1

### 9. Which task appears most often in system_small.log?

![alt text](image-7.png)

**Explanation** Same as task 7 but different file name and field 4 instead of 5
