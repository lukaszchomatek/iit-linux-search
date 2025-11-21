> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

Example:

![task 0](task0.png)

**Explanation** Write the explanation why the specific command was used.

Example: wc command is to count data in a given file. -l parameter is for counting lines.

### 1. How many lines in access_small.log have path /login?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** grep found text in lines and passed it to wc which counted it 

---<img width="1084" height="101" alt="1-1" src="https://github.com/user-attachments/assets/1bca06fa-eeaf-4a92-a933-0a842269221d" />


### 2. How many occurrences of Smith are in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** grep found text in lines and -o made all occurance separate and wc counted it

<img width="1097" height="50" alt="1-2" src="https://github.com/user-attachments/assets/c639565d-573e-4923-af7d-cc1d5eff782d" />


### 3. How many occurrences of Smith are in fullnames_simple.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

**Explanation** Write the explanation why the specific command was used.

### 4. Which age is most frequent in fullnames_with_age.txt?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="1092" height="78" alt="1-4" src="https://github.com/user-attachments/assets/e1f95b67-f958-4cd6-8ce1-c6322ddb9339" />

**Explanation** grep found age of every person than sorted it, counted how many times each age appeard, sorted highest first, showed first

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="1087" height="271" alt="1-5" src="https://github.com/user-attachments/assets/949af3db-9c21-4e89-8624-2a0cf38e7d73" />


**Explanation** awk printed first and second field (name, surname), sorted all names alphabeticaly, counted how many times each names appeard, sorted highest first, showed first 10

### 6. How many unique users are in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="1087" height="71" alt="1-6" src="https://github.com/user-attachments/assets/4f884393-9820-4864-9d66-482f63d67e92" />


**Explanation** grep found usernames, sorted them, removed duplicates and counted.

### 7. Which status code appears most often in access_medium.log? 

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="1094" height="75" alt="1-7" src="https://github.com/user-attachments/assets/0577bcda-e647-48c7-9ab8-3f6d2ab89daa" />


**Explanation** awk extratcted status code, sorted them, counted occurance, sorted by frequency (highest first), showed most fequent

### 8. What is the top 3 most common modules in app_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="841" height="116" alt="1-8" src="https://github.com/user-attachments/assets/e935ca70-b65a-4a13-984a-2534b0ab4382" />


**Explanation** awk extratcted module names, sorted them, counted occurance, sorted by frequency (highest first), showed 3 most fequent


### 9. Which task appears most often in system_small.log?

Put screenshot from Codespaces illustrating the result here.
Correct screenshot should contain your github username in the shell, a command and the result.

<img width="971" height="77" alt="1-9" src="https://github.com/user-attachments/assets/0671c4aa-1622-4f2c-8d5b-4f73a51b3f03" />


**Explanation** grep found task names, sorted them, counted occurances, sorted by frequency(highest fist), showed most frequent task
