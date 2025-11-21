> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

// TODO: Task1.png

**Explanation:** We use grep to filter out all lines that do not contain /login, then we count the lines that remain. Since no other column can contain /login, it's not required to separate them apart. 

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

// TODO: Task2.png

**Explanation:** We use grep again to check for "Smith" occurances in the file (assuming there's no "Smith Smith") and then we count the lines. 

### 3. How many occurrences of Smith are in fullnames_simple.txt?

// TODO: Task3.png

**Explanation:** File doesn't exit.

### 4. Which age is most frequent in fullnames_with_age.txt?

// TODO: Task4.png

**Explanation:** File is separated into columns with " " (spaces) so first we cut it respect to this and take 3rd column with is formated as for eg.: "age=18", so we cut it again in respect to "=" and take 2nd column.
Afterwards sort it, then group and count them using uniqe. Unique appends the amount of occurences in front of the argument it checked the occurence of, so we sort it again, this time in reverse order (decreasing) and we have the: [amount of occurences][age] from most frequent to least frequent.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

// TODO: Task5.png

**Explanation:** First we separate names from the ages by taking everything before the "," with cut, then we sort the name and count them with uniq, after we sort the uniq result in decreasing order. To limit the results to 10 we just use head command.

### 6. How many unique users are in app_small.log?

// TODO: Task6.png

**Explanation:** First we fix the file, since some lines had double spaces, which can cause trouble in the results. We cut the data twice to leave just the users which are: "systsem", "guest" or "u[number identifier]". Then we sort them and uniq them WITHOUT counting them. Then we count the resulting lines. 

### 7. Which status code appears most often in access_medium.log? 

// TODO: Task7.png

**Explanation:** We cut data and take only html status code column, then we sort and count each error occurence count using unique and we display the result in descending order. Most common error code is "500".

### 8. What is the top 3 most common modules in app_small.log?

// TODO: Task8.png

**Explanation:** We cut date in respect to spaces and take only 3rd column. Then we sort, uniq count it, then sort descending again and limit displayed results to 3.

### 9. Which task appears most often in system_small.log?

// TODO: Task9.png

**Explanation:** We cut the file and take the 4th column, then we cut out the "task=" but it's not required. After sorting the result we uniq count it and sort in descending order. Top result is the task that appears most often.
