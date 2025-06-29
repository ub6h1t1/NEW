Regex Basics (Regular Expressions)
Regular expressions are patterns used to match character combinations in text.

Common Regex Symbols
Symbol	Meaning	Example
.	Matches any single character	a.c → matches abc, acc
^	Matches beginning of line	^abc → lines starting with abc
$	Matches end of line	abc$ → lines ending with abc
*	Matches 0 or more of preceding char	bo* → b, bo, boo
+	Matches 1 or more of preceding char	bo+ → bo, boo
[]	Matches any one of characters	[aeiou] → vowels
[^]	Negation	[^0-9] → non-digits
{}	Number of occurrences	a{2,4} → aa, aaa, aaaa
`	`	OR operator
()	Grouping	(ab)+ matches ab, abab, etc.

🧰 grep – Search Text Using Patterns
Syntax:
grep [OPTIONS] PATTERN [FILE...]
Examples:
grep "hello" file.txt         # Matches lines with 'hello'
grep -i "hello" file.txt      # Case-insensitive match
grep -r "main" .              # Recursively search in all files in current dir
grep -n "error" log.txt       # Show line numbers
grep -v "test" file.txt       # Show lines that do NOT contain 'test'
🛠️ sed – Stream Editor for Filtering and Transforming Text
Syntax:
sed [OPTIONS] 'COMMAND' [FILE]
Examples:
sed 's/old/new/' file.txt       # Replace first occurrence of 'old' with 'new'
sed 's/old/new/g' file.txt      # Replace all occurrences on a line
sed -n '5,10p' file.txt         # Print lines 5 to 10
sed '/pattern/d' file.txt       # Delete lines matching pattern
sed '2d' file.txt               # Delete 2nd line
📊 awk – Pattern Scanning and Processing Language
Syntax:
awk 'pattern {action}' [file]
Examples:
awk '{print $1}' file.txt           # Print 1st column
awk '/error/ {print $2}' log.txt    # Print 2nd field where 'error' appears
awk '{sum += $1} END {print sum}' numbers.txt   # Sum values in 1st column
awk 'NR==1,NR==3' file.txt          # Print lines 1 to 3
Conclusion
grep is useful for searching log files, filtering command output, or quickly finding specific information within file
sed is often used in scripting and batch processing to modify text files and automate text transformations.
awk is handy for data extraction, report generation, and data manipulation tasks involving structured text or CSV-like data.
Regex mastery will make you much more efficient at text processing and parsing in Linux!
