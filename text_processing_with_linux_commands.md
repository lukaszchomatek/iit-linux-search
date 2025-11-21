> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Commmand ``wc`` is used to count lines, words, characters and bytes in a file, and ``-l`` narrows it only to lines.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 1](task1.png)

**Explanation** Command ``grep`` is used to search for text and ``-c`` counts the matched lines.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 2](task2.png)

**Explanation** Command ``grep`` is used to search for text and ``-c`` counts the matched lines.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 3](task3.png)

**Explanation** There isn't any file called ``fullnames_simple.txt``. ``find /`` searches recursively from the root and ``-name`` looks for specific filename. ``2>/dev/null`` is just to hide "Permission denied" error.

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 4](task4.png)

**Explanation** ``grep -o "age=[^ ]*" /workspaces/iit-linux-search/names/fullnames_with_age.txt`` all fragments that starts with ``age=`` to the first space. ``cut -d "=" -f 2`` it splits a line by "=" and only takes second value (that is the age id in this case). ``sort`` is being used to group these numers and ``uniq -c`` to count how many of them there are. Than ``sort -nr`` sorts them by the occurance and ``head -1`` shows the winner.

### 5. Show the 10 most common names (first+last) in fullnames_with_age.txt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 5](task5.png)

**Explanation** ``awk -F "," '{print $1}' /workspaces/iit-linux-search/names/fullnames_with_age.txt`` splits each line by sign "," and gets the first part. ``sort`` is being used to group these names and ``uniq -c`` to count how many of them there are. Than ``sort -nr`` sorts them by the occurance and ``head -1`` shows the winner.

### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 6](task6.png)

**Explanation** ``grep -o "user=[^ ]*" /workspaces/iit-linux-search/logs/app_small.log`` find all fragments that starts with ``user=`` to the first space. ``cut -d "=" -f 2`` it splits a line by "=" and only takes second value (that is the user id in this case). ``sort | uniq | wc -l`` sorts them, deletes duplicates and counts them.

### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 7](task7.png)

**Explanation** ``awk '{print $5}' /workspaces/iit-linux-search/logs/access_medium.log`` takes the 5th collumn. ``sort | uniq -c | sort -nr | head -1`` sorts them, counts unique, sorts them by occurance and gets the first one.

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 8](task8.png)

**Explanation** ``awk '{print $3}' /workspaces/iit-linux-search/logs/app_small.log`` takes the 3rd collumn. ``sort | uniq -c | sort -nr | head -1`` sorts them, counts unique, sorts them by occurance and gets the top 3.

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

![task 9](task9.png)

**Explanation** ``grep -o "task=[^ ]*" /workspaces/iit-linux-search/logs/system_small.log`` find all fragments that starts with ``task=`` to the first space. ``cut -d "=" -f 2`` it splits a line by "=" and only takes second value (that is the task in this case). ``sort |uniq -c | sort -nr | head -1`` sorts them, deletes duplicates, sorts by te ocurrance and gets the first one
