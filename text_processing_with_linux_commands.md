> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?
![alt text](task1.png)

**Explanation** Write the explanation why the specific command was used.

    grep filters lines containing /login and wc counts how many are there.
---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![alt text](task2.png)

**Explanation** Write the explanation why the specific command was used.

grep check if line contains "Smith" wc counts those lines. As it is surname it wont apear twice in one line.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

This file doesn't exist.

**Explanation** Write the explanation why the specific command was used.

### 4. Which age is most frequent in fullnames_with_age.txt?

![alt text](task4.png)

**Explanation** Write the explanation why the specific command was used.
first cut extracts age from each line(it's always after "=") then I sort(sort -r sorts in reverse order) and count unique(uniq -c counts inuque items and amount of them) ones. The rest is for clearer reading.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![alt text](task5.png)

**Explanation** Write the explanation why the specific command was used.
I cut the names then sort uniq sort which returned sorted list with number of apperance. head dispalys 10 top

### 6. How many unique users are in app_small.log?

![alt text](task6.png)

**Explanation** Write the explanation why the specific command was used.
I cut out the line part after after "=" and then before space so it's only age which I sort and get uniques.

### 7. Which status code appears most often in access_medium.log? 

![alt text](task7.png)

**Explanation** Write the explanation why the specific command was used.
I cut out the specifique number then sort and find unique and sort to find the biggest.

### 8. What is the top 3 most common modules in app_small.log?

![alt text](task8.png)

**Explanation** Write the explanation why the specific command was used.
I extract the column wuth modules then sort them, find uniques and dispaly sorted ones.

### 9. Which task appears most often in system_small.log?

![alt text](task9.png)

**Explanation** Write the explanation why the specific command was used.

I extract and count each one then display them.