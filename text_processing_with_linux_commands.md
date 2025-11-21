<img width="866" height="51" alt="obraz" src="https://github.com/user-attachments/assets/896eaa85-60f6-4573-a4e3-52237444bcf5" />> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?
<img width="789" height="34" alt="obraz" src="https://github.com/user-attachments/assets/b8d320d2-40c5-4eec-8d14-405eedb5cf6e" />

**Explanation** The grep command filters the file for lines containing the specified pattern, | passess the output to the following command and wc with -l parameter counts the lines.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?
<img width="760" height="37" alt="obraz" src="https://github.com/user-attachments/assets/f831eb2a-8f6f-499e-81bc-fb923f6895dd" />

**Explanation** The same as the previous one only the pattern and file changed.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

<img width="858" height="51" alt="obraz" src="https://github.com/user-attachments/assets/058331c5-451a-4fc9-9362-ad9c5d20a07f" />

**Explanation** Same as before, but the file fullnames_simple.txt doesn't exist.

### 4. Which age is most frequent in fullnames_with_age.txt?

<img width="1134" height="44" alt="obraz" src="https://github.com/user-attachments/assets/6f75e5e3-8b77-4593-880b-bce643a08cf4" />

**Explanation** cut -d ' ' splits the text by the delimeter ' ' -f 3 parameter selects the third field, second cut splits the text by '=' and selects second field, sort sorts the data, uniq -c counts occurrence of each age, sort -nr sorts the counts numerically in reverse | head -1 duisplays only the firs line.

### 5. Show the 10 most common names (first+last) in fullnames_with_age.txt.

<img width="1190" height="189" alt="obraz" src="https://github.com/user-attachments/assets/5ff2b046-f79e-4f46-aebe-f3dcd02b50c1" />


**Explanation** same as before but witch different data.

### 6. How many unique users are in app_small.log?
<img width="1061" height="35" alt="obraz" src="https://github.com/user-attachments/assets/2658543c-3c70-4f18-8618-98add5c98b72" />

**Explanation** cut commands format the data, uniq shows only unique linse and wc -l counts them.

### 7. Which status code appears most often in access_medium.log? 
<img width="866" height="51" alt="obraz" src="https://github.com/user-attachments/assets/f5b9d889-2646-431f-8eed-6b16c46ae9c7" />



**Explanation** Write the explanation why the specific command was used.

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.
