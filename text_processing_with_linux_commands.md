> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

<img width="673" height="37" alt="obraz" src="https://github.com/user-attachments/assets/f981fb6a-3a87-4b30-9346-7ad46b9b9ef5" />

**Explanation** grep was filtering lines containing "/login" and "wc -l" was used to count the lines. 

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

<img width="715" height="35" alt="obraz" src="https://github.com/user-attachments/assets/87aaeb82-3650-412d-979b-6d24c0653ca8" />

**Explanation** grep was filtering lines containing "Smith" and "wc -l" was used to count the lines. 

---

### 3. How many occurrences of Smith are in fullnames_simple.txt?

I can not see a file fullnames_simple.txt. 

---

### 4. Which age is most frequent in fullnames_with_age.txt?

<img width="807" height="61" alt="obraz" src="https://github.com/user-attachments/assets/896bc5fc-b9bf-4395-ad67-97f9134d9649" />


**Explanation** cut-d was used to extract 'age= x' part from the lines. Then cut -d was used to extract only 'x' part. Sortwas used to sort the values, what is required for uniq. Uniq wasused to count unique occurences, sort -nr was used to sort with reversed order, head -1 was used to show just TOP 1 answer.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

<img width="956" height="191" alt="obraz" src="https://github.com/user-attachments/assets/7b763e7f-2259-4c52-a8dd-c731926970f7" />

**Explanation** cut -d was used to separate full names out of the lines, then sort because it's required for uniq, then uniq to count unique occurences, sort -rn to sort numerically with reversed order, and then head -10 to show just the top 10. 

### 6. How many unique users are in app_small.log?

<img width="914" height="38" alt="obraz" src="https://github.com/user-attachments/assets/06a604a0-4dff-4da9-a24d-0c74e46da095" />

**Explanation** cut -d was used to separate 'u15 action' from each line, cut -d wasused to separate 'ux' from each line, sort was used because it's required for uniq, uniq was used to count occurences, wc -l was used to count number of users.

### 7. Which status code appears most often in access_medium.log? 

<img width="910" height="40" alt="obraz" src="https://github.com/user-attachments/assets/dd09aa0c-aa79-4aa4-9aac-38d4ae3a0db1" />

**Explanation** cut -d was used to separate '5th' part from each line, sort was used because it's required for uniq, uniq was used to count unique occurences, sort -nr was used to sort with reversed order and head -1 wasused to show just the top 1 code status.

### 8. What is the top 3 most common modules in app_small.log?

<img width="879" height="72" alt="obraz" src="https://github.com/user-attachments/assets/fde3e3ea-0742-4a65-82d8-c224619b1598" />

**Explanation** cut -d was used to separate the modules from each line, then sort was used because it's required for uniq, then sort -nr was used to sort with reversed order, and then head -3 was used to show only TOP 3 modules. 

### 9. Which task appears most often in system_small.log?

<img width="1029" height="40" alt="obraz" src="https://github.com/user-attachments/assets/dd8b90b2-e120-41ed-a9be-a969fcebcde7" />

**Explanation** cut -d was used to separate 'task=x' part from each line, cut -d was used to remove the 'task=' part, sort was used because it's required for uniq, sort -nr was used to sort with reversed order head -1 was used to show only top 1 task. 
