> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![task1](image.png)
**Explanation** We get the lines that start with "/login" using grep, then we pass the output into wc, which counts all lines (beacause -l).

---

### 2. How many different ages are in fullnames_with_age.txt?

![task2](image-1.png)

**Explanation** by cut -d "," we get only the part with something, the age and "=", then we get only the age by another cut -d "=". After that, we sort the output so that we can get unique values, and then we count them :).

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task3](image-2.png)

**Explanation** By cut " " we only get the column with first names, then we sort them so that we can then use uniq. After all this operations we simply count the lines.

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task4](image-3.png)

**Explanation** We do kind of similar searching, such as in second example, however this time we sort the ages, then we obtain 2 columns: one with ages count, second one with ages (by using uniq -c). After, we sort by numbers and reversed, so that we get the age with the most appearances in the text as the first record, then by head we get the record. Age 56 appeared 222 in the text.

---

### 5. Which username failed login most often in auth_small.csv?

![task5](image-4.png)

**Explanation** Here, we use similar logic as in previous example. We use grep to get only the users who failed, then cut so we get only usernames, we sort the output, then get the unique names and count of their appearances, again sort to get the highest value and finally head to get the head :).

---

### 6. How many lines in system_small.log have ok=true?

![task6](image-6.png)

**Explanation** By grep we get lines only with "ok=true", then simply count the lines.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task7](image-7.png)

**Explanation** We cut firstly so that we get only the part with level=..., then we cut once more to obtain only the level (error/etc.). Now we sort the values in order to use uniq, then we sort those unique appearences by numbers and lastly we obtain only the first line (using head) which gives us the most apperances in the text.

---

### 8. What is the top 3 most common actions in app_small.log?

![task8](image-8.png)

**Explanation** We cut two times, firstly we get the fragment action=something, then we get only the part after "=". Now we sort the values in order to use uniq -c, then with this output we sort it by numbers and reversed. Now we simply use head to obtain the 3 biggest numbers.

---

### 9. How many unique users are in app_small.log?

![task9](image-9.png)

**Explanation** Firstly, we cut to get only the part with user=something, then we cut once again to get only the user id. Now we can sort it in order to use the uniq, which gives us all unique user ids. Now we simply use wc -l to count the lines.


---