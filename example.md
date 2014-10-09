

Exercise 6 - Word Count
=========
[Exercise Concepts](#concepts)<br/>
[Solution](#solution)<br/>
[Alternatives](#alternatives)<br/>
[Extensions](#extensions)<br/>

###<a name=concepts>Exercise Concepts</a>
- Dictionaries
    - Key/value store
    - difference between dict and list
    - how to access a dict value
    - why dict is more efficient than a list
    - `.get()`
    - `.setdefault()`
- Reading a file
    - parsing command line arguments
    - navigating to a file path with python
    - file object
    - read vs open 
    - ETCETERA
 
 
.



###<a name=solution>Exercise Solution</a>

#####"Ideal" Solution
```python
# the example solution would go here
# inside a code block
# code blocks are made by surrounding some lines with triple backticks(`)


ifrom sys import argv
import re

script, filename = argv 	#1

f = open(filename)
text = f.read()
f.close() 					#2

lower_text = text.lower()
lower_text = re.sub('[!_.,?""''\];:\'\-\()--]', ' ', lower_text)
list_of_strings = lower_text.split()
word_dict = {}

for item in list_of_strings:
  word_dict[item] = word_dict.get(item, 0) + 1  #3

list_of_tuples = word_dict.items()

#sorts by value
second_list_of_tuples = sorted(list_of_tuples, 
                 key=lambda word_dict : word_dict[0], 
                 reverse=False )
#sorts by key
final_sorted_list_of_tuples =sorted(second_list_of_tuples, 
                  key=lambda second_list_of_tuples: 
                  second_list_of_tuples[1] )

print final_sorted_list_of_tuples

```
1. get command line arguments
2. make sure to close file
3. use get method instead of if/else block
4. etc
.

 
####<a name=alternatives>Alternative solutions</a>
>#####Using an if/else block instead of .get method
>```python
>if key in dict:
>    dict[key] += 1 
>else
>    dict[key] = 1
>```
>Pros:
>- may be easier to understand
>Cons:
>    - less efficient
>    - takes up more space

 .


>#####Using try/except instead of .get method
>```python
>try:
    dict[key] += 1 
except KeyError
    dict[key] = 1
```
>Pros:
>- Are there pros to this?
>Cons:
>    - Probably don't understand what exceptions or KeyError is
>   

.

####<a name=extensions>Extensions</a>
1. lowercasing words and strip() or custom method of removing
>`text.lower()`

2. punctuation before counting (some people found string.punctuation or regular expressions)
>`lower_text = re.sub('[!_.,?""''\];:\'\-\()--]', ' ', lower_text)` 

3. sort dictionary values
>`ordered = sorted(list_of_tuples, key=lambda tup : tup[0], >reverse=False )`
4. use some kind of lambda with sorting function to sort by frequency and then alphabetically
5. itemgetter?
6. write a sort function
