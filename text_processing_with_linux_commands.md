> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.


![task 0](image-1.png)


wc command is to count data in a given file. -l parameter is for counting lines. names/fullnames_with_age.txt represents location of a file.



### 1. How many lines in access_small.log have path /login?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
![task1](image-2.png)

grep comand is used to search for specific paterns in text, "-c" counts the amount of occuring, "/login" is the text we are looking for  and logs/access_small.log is a file in which we are searching 

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?
![tesk 2](image-3.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
grep comand is used to search for specific paterns in text, "-c" counts the amount of occuring, "Smith" is the text we are looking for  and names/fullnames_with_age.txt is a file in which we are searching 

### 3. How many occurrences of Smith are in fullnames_simple.txt?

![tesk 3](image-3.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
grep comand is used to search for specific paterns in text, "-c" counts the amount of occuring, "Smith" is the text we are looking for  and names/fullnames_with_age.txt is a file in which we are searching

### 4. Which age is most frequent in fullnames_with_age.txt?

![task 4](image-4.png)
Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

awk proceses text by fields, $NF takes onyl the last field in the line.we use that because age is the lst piece of information in the file, | sort sorting the age groups,  |unique -c counts unique age groups, |sort -nr sorts it numericaly and reverses it so the most frequent is on the top of the list | head -1 shows only the first line of already sorted list so we get the right output

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![task 5](image-5.png)
Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
We used cut -d' ' -f1,2 to extract just the first and last names from each line. Then sort was used to arrange the names alphabetically so that duplicates are next to each other. After that, uniq -c counted how many times each name appeared. sort -nr was applied to order the counts from highest to lowest, and finally, head -10 was used to display only the top 10 most common names.


### 6. How many unique users are in app_small.log?

![task 6](image-6.png)
Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
grep -o 'user=[^ ]*' — extracts all occurrences of user=… from the log.
sort -u — sorts the results and removes duplicates, keeping only unique users.
wc -l — counts the number of lines, giving the total number of unique users.


### 7. Which status code appears most often in access_medium.log? 

![task 7](image-7.png)
Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

awk '{print $5}' — extracts the 5th field from each line, which is the HTTP status code.
sort — sorts the codes so duplicates are next to each other.
uniq -c — counts how many times each code appears.
sort -nr — sorts the counts in descending order.
head -1 — shows only the most frequent status code. the answer contents the amounnt of occurances and the status code iteslf , first number beeing ocurances and second beeing status code.
### 8. What is the top 3 most common modules in logs/app_small.log?

![task 8](image-8.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

awk '{print $3}' — extracts the 3rd field from each line, which is the module name.
sort — sorts the module names 
uniq -c — counts how many times each module appears.
sort -nr — sorts the counts in descending order.
head -3 — shows the top 3 most common modules.
### 9. Which task appears most often in system_small.log?

![task 9](image-9.png)

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

rep -o 'task=[^ ]*' — extracts all occurrences of task=….
sort — sorts them 
uniq -c — counts each unique task.
sort -nr — sorts counts in descending order.
head -1 — shows the task that appears most often.

