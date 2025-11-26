> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

![Task 1](task1.png)

1. `grep` - Get lines that only contain "/login" in the file
2. `wc` - Count the lines that `grep` returned and print the count
   - `-l` - Only show line count

---

### 2. How many different ages are in fullnames_with_age.txt?

![Task 2](task2.png)

1. `grep` - Extract age parameters(?) from the file
   - `-o` - Get only the matched parts, not the whole line
   - `"age=[0-9]*"` - A regexp that matches only the age part
2. `sort` - Sort the ages to remove duplicates
   - `-u` - Retain only unique ages (like `uniq`)
3. `wc` - Count the filtered ages and print the count
   - `-l` - Only show line count

---

### 3. How many unique first names are in fullnames_with_age.txt?

![Task 3](task3.png)

1. `grep` - Extract only the first names from the file
   - `-o` - Get only the matched parts, not the whole line
   - `"^[a-zA-Z]* "` - A regexp that only matches the first name
2. `sort` - Sort the names to only contain distinct names
   - `-u` - Retain unique names only
3. `wc` - Count the resulting names and print the count
   - `-l` - Only show the line count

---

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 5. Which username failed login most often in auth_small.csv?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 6. How many lines in system_small.log have ok=true?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 8. What is the top 3 most common actions in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---

### 9. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

---