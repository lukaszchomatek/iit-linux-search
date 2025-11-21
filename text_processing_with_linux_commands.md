> This is the demonstration how to use Linux commands to process strutured text data.

### 0. How many lines are in fullnames_with_age.txt?

![alt text](image.png)

**Explanation** The wc command counts data in a file. The -l flag means "count lines".

### 1. How many lines in access_small.log have path /login?

![alt text](image-1.png)

**Explanation** The grep command searches for lines matching a pattern. We search for /login.The output is piped to wc -l to count the number of matching lines.

---

### 2. How many occurrences of Smith are in fullnames_with_age.txt?

![alt text](image-2.png)

**Explanation** grep -o prints only matched occurrences. Counting them with wc -l gives the number of times “Smith” appears.

### 3. How many occurrences of Smith are in fullnames_simple.txt?

![alt text](image-2.png)

### 4. Which age is most frequent in fullnames_with_age.txt?

![alt text](image-3.png)

**Explanation** awk '{print $NF}' prints the last field (age).
sort groups identical ages together.
uniq -c counts occurrences.
Final sort -nr shows most frequent first.
head -1 picks the top result.

### 5. Show the 10 most common names (first+last) in fullnames_with_agetxt.

![alt text](image-4.png)

**Explanation** awk '{print $1, $2}' extracts first and last name.
Sorting + uniq -c counts occurrences.
sort -nr sorts by frequency.
head -10 shows top 10.

### 6. How many unique users are in app_small.log?

![alt text](image-5.png)

**Explanation** awk '{print $2}' extracts the username column.
sort | uniq removes duplicates.
wc -l counts unique usernames.

### 7. Which status code appears most often in access_medium.log? 

![alt text](image-9.png)

**Explanation** The awk '{print $5}' command extracts the 5th column from each log line, which contains the HTTP status code.
Then sort | uniq -c counts how many times each code appears.
Finally, sort -nr | head -1 shows the most frequent status code.

### 8. What is the top 3 most common modules in app_small.log?

![alt text](image-7.png)

**Explanation** awk '{print $3}' extracts the module name field.
uniq -c counts them.
head -3 gives the top 3.

### 9. Which task appears most often in system_small.log?

![alt text](image-8.png)

**Explanation** Extract the task field, sort, count, show the most common.
