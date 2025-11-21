> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![first command](image.png)

grep would display lines in which there is "/login" and -c counts them 

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![alt text](image-2.png)

grep -c counts each occurance of "Smith"

### 3. How many occurrences of Smith are in fullnames_simple.txt?

(original file does not exist, redo of ezercise 2)

![alt text](image-3.png)

grep -c counts each occurance of "Smith"

### 4. Which age is most frequent in fullnames_with_age.txt?

![alt text](image-1.png)

I've searched on the internet and came onto this resource 
https://unix.stackexchange.com/questions/136884/how-to-use-a-shell-command-to-only-show-the-first-column-and-last-column-in-a-te
and then went with the awk  

awk '{prinf $NF}' prints the last column of the file, sort sotrs them, uniq -c counts the ammount of each unique age, sort -r sorts them by descending order and head -1 displays only the first element and in case the age occuring the most frequently

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![alt text](image-4.png)

awk ... selects the names and surnames from the file, we sort them, count occurances of each unique combination, sort them decreasing, and head displays 10 by default, so they are top 10 occurances

### 6. How many unique users are in app_small.log?

![alt text](image-5.png)

we select the user column using awk limited by spaces sort them select unique ones and count lines using wc -l so we have 22

### 7. Which status code appears most often in access_medium.log? 

![alt text](image-6.png)

status codes are in 5-th column we select them sort them, count unique ones, sort them in descending order and display the one occuring the most offen (status code 500 occuring 1751 times)

### 8. What is the top 3 most common modules in app_small.log?

![alt text](image-9.png)

awk blah balh blah 

### 9. Which task appears most often in system_small.log?

![alt text](image-7.png)

the same but with different file and column so I don't want to write the explanation once again