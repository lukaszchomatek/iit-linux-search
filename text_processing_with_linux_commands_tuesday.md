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

![task1](task1.png)

**Explanation** Write the explanation why the specific command was used.
At begining I search for lines containg "/login" and then i count number of these elements

---

### 2. How many different ages are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](task2.png)

**Explanation** Write the explanation why the specific command was used.
I search for phrase age=something then I cut age= I sort it then remove duplicates and then print number of uniq elements

---

### 3. How many unique first names are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](task3.png)

**Explanation** Write the explanation why the specific command was used.

I cut first column with names then sort it and remove duplicated as in previous task

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](task4.png)

**Explanation** Write the explanation why the specific command was used.
So i cut names and surnames then i cut age= so I got only numbers and then i sort it after that remove dupilcates but couting it then sort decreasing and finally print the highest value (first one)

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![alt text](task5.png)

**Explanation** Write the explanation why the specific command was used.

I only search in lines which contains "FAIL" then i remove everything except usernames after that I do everything what i have done in previous sorting
---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.
![alt text](task6.png)

**Explanation** Write the explanation why the specific command was used.
so I search for this keyword and count how many it appears
---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image.png)

**Explanation** Write the explanation why the specific command was used.
I cut to phrase level=sth then only to sth and after that I just sort and count like before
---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-1.png)

**Explanation** Write the explanation why the specific command was used.
So I cut everytihng except actions and then i sort  it as before and print top 3 actions
---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![alt text](image-2.png)

**Explanation** Write the explanation why the specific command was used.
I remove everything except usernames I sort it remove duplicates and count how many are of them

---