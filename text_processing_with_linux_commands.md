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

![alt text](image.png)

**Explanation** Command grep was used because it finds all line in "access_small.log" that contain "/login"

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-1.png)

**Explanation** grep -c was used because it counts all lines in "fullnames_with_age.txt" that contain "Smith"

### 3. How many occurrences of Smith are in fullnames_simple.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-1.png)

**Explanation** grep -c was used because it counts all lines in "fullnames_with_age.txt" that contain "Smith"

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-8.png)

**Explanation** cut cuts the 3rd field, sort sorts the output, uniq count all unique appearances, sort -nr sorts the output from highest to lowest numerically and head -1 shows the top result

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-3.png)

**Explanation** cut removes "," and then rest is like above except we show top 10 results

### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-4.png)

**Explanation** cut cuts the fourth field, sort sorts the output, uniq merges outputs so all are unique and wc -l counts how many times they appear

### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-5.png)

**Explanation** cut cuts the fifth field, sort sorts the output, uniq count all unique appearances, sort -nr sorts the output from highest to lowest numerically and head -1 shows the top result

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-6.png)

**Explanation** Almost the same as the example above but we show the top 3 results

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-7.png)

**Explanation** Similiar as 7  and 8 we show the first result
