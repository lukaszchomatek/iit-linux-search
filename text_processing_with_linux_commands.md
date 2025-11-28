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

**Explanation** cut commands format the data, uniq shows only unique lines and wc -l counts them.

### 7. Which status code appears most often in access_medium.log? 
<img width="982" height="32" alt="{376F5850-7575-4DAE-A3BE-9F2A7EE9BB15}" src="https://github.com/user-attachments/assets/db0f73c3-4137-4248-b56d-493545fbbfe8" />




**Explanation** same as previous examples.

### 8. What is the top 3 most common modules in app_small.log?

<img width="1003" height="73" alt="{3A9647B6-2505-4AE4-ABD4-352A688F9CD5}" src="https://github.com/user-attachments/assets/5600268e-aae7-4f2a-8c84-4af1d58ff4ba" />


**Explanation** Similar to previous tasks but tr -s ' ' is used to get rid of the double whitespaces.

### 9. Which task appears most often in system_small.log?
<img width="1087" height="41" alt="{5DD43B43-5399-4734-9E1C-CE1A7377F9EF}" src="https://github.com/user-attachments/assets/258fb71d-75fb-4387-aa99-506e890abdd0" />


**Explanation** Weird data but using = as delimeter works fine.
