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

![Task 4](task4.png)

1. `grep` - Extract ages from the file
   - `-o` - Get only the matched parts, not the whole line
   - `"age=[0-9]*"` - Regexp that matches only the age parts
2. `sort` - Sorts input for `uniq`
3. `uniq` - Count unique ages
   - `-c` - Additionally print the counted ages
4. `sort` - Sort the counted ages
   - `-n` - Sort by numerical values
   - `-r` - Sort from highest to lowest count
5. `head` - Show only the most frequent age
   - `-n 1` - Show only the first line of the `sort` output

---

### 5. Which username failed login most often in auth_small.csv?

![Task 5](task5.png)

1. `cut` - Get only the username and result column from file
   - `-d ","` - Set the delimiter to ","; not TAB
   - `-f "2,4"` - Select column 2 and 4, which are the username and result columns
2. `grep` - Filter the results to only contain failures
3. `sort` - Sort the results for `uniq`
4. `uniq` - Get counts for each unique entry (Only usernames are different at this point)
   - `-c` - Count the amount of duplicates
5. `sort` - Sort the results to find the most often failed login
   - `-n` - Sort by numerical values
   - `-r` - Sort from highest to lowest
6. `head` - Show the most often login failure with username
   - `-n 1` - Show only the first line of the results, sorted by the `sort`

---

### 6. How many lines in system_small.log have ok=true?

![Task 6](task6.png)

1. `grep` - Get only lines in the file that have "ok=true"
2. `wc` - Print the line count
   `-l` - Count lines, not words

---

### 7, Which level (INFO, WARN, ERROR) appears most often in system_small.log?

![Task 7](task7.png)

1. `grep` - Get the level from each line (`cut`'s output isn't reliable, because the file is a little damaged)
   - `-o` - Only get the matched parts, not the whole line
   - `"level=[A-Z]* "` - Regexp to match only the level part
2. `sort` - Sort the results for `uniq`
3. `uniq` - Count occurences for each unique level
   - `-c` - Print counts for each level
4. `sort` - Sort the results to find the most often logged level
   - `-n` - Sort by numerical values
   - `-r` - Sort from highest to lowest
5. `head` - Print the most often used level
   - `-n 1` - Show only the first line of the results

---

### 8. What is the top 3 most common actions in app_small.log?

![Task 8](task8.png)

1. `grep` - Get the action from each line (`cut`'s output is rarely unreliable for unknown reason)
   - `-o` - Only get the matched parts, not the whole line
   - `"action=[A-Za-z]* "` - Regexp to match only the action part
2. `sort` - Sort the results for `uniq`
3. `uniq` - Count occurences for each unique action
   - `-c` - Print counts for each action
4. `sort` - Sort the results to find the most often used action
   - `-n` - Sort by numerical values
   - `-r` - Sort from highest to lowest
5. `head` - Print the most often used actions
   - `-n 3` - Show only the first three lines of the results

---

### 9. How many unique users are in app_small.log?

![Task 9](task9.png)

1. `grep` - Get the user part from each line (`cut`'s output is rarely unreliable for unknown reason)
   - `-o` - Only get the matched parts, not the whole line
   - `"user=[A-Za-z0-9]* "` - Regexp to match only the user part
2. `sort` - Sort and remove duplicates from the result
   - `-u` - Remove duplicates (like `uniq`)
3. `wc` - Print number of unique users from result
   - `-l` - Count lines, not words

---