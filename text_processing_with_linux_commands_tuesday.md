> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 0](task0.png)

**Explanation** word count with flag -l count all lines in path

Example: wc command is to count data in a given file. -l parameter is for counting lines.

---

### 1. How many lines in access_small.log have path /login?

![task 1](task1.png)

**Explanation** grep filters all files for "/login" path and then use wc to count them

---

### 2. How many different ages are in fullnames_with_age.txt?

![task 2](task2.png)


**Explanation** cut line and search for "=", sort groups the numbers, uniq removes duplications, wc counts that unique ages

---

### 3. How many unique first names are in fullnames_with_age.txt?

![task 3](task3.png)

**Explanation** cut search for first field -f1 with space " ". Sort groups the numbers, uniq removes duplications, wc counts that unique ages

---

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](task4.png)

**Explanation** cut grabs age and sorted it. uniq -c counts how many times each age appear. Then check frequency and write down frequency and which age is most freqent.

---

### 5. Which username failed login most often in auth_small.csv?

![task 5](task5.png)

**Explanation** grep is looking for "fail" in file, cut grabs the name of user, then sort them and checks with user failed login most often

---

### 6. How many lines in system_small.log have ok=true?

![task 6](task6.png)

**Explanation** grep is filtering for "ok=true", then wc sum them up and writes down result

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![task 7](task7.png)

**Explanation** grep -oE grabs only matching words, then command sort them remove duplication, sum them sup and write down which level appears most often.

---

### 8. What is the top 3 most common actions in app_small.log?

![task 8](task8.png)

**Explanation** cat open file, "tr -s" is for making multiple spaces into one, cut to grab action in column 5 in file, sort and unique for sorting and removing duplications.
sort -nr | head -n 3 finds top 3 most common actions

---

### 9. How many unique users are in app_small.log?

![task 9](task9.png)

**Explanation** cat open file, "tr -s" is for making multiple spaces into one, cut grabs column number 4, sort and unique for sorting and removing duplications. Then wc sum it up and write down result


---