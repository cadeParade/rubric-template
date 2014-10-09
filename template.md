

Exercise 6 - Word Count
=========
[Exercise Concepts](#concepts)<br/>
[Solution](#solution)<br/>
[Alternatives](#alternatives)<br/>
[Extensions](#extensions)<br/>

###<a name=concepts>Exercise Concepts</a>
- Big Concept 1
    - A part of the concept that is important
    - another important thing

- Big Concept 2
    - sub concept
    - sub concept
 
.



###<a name=solution>Exercise Solution</a>
[Link to exercise directions](https://github.com/hackbrightacademy)

#####"Ideal" Solution
```python
# the example solution would go here
# inside a code block

ifrom sys import argv
import re

script, filename = argv 	#1

f = open(filename)
text = f.read()
f.close() 					#2


```
1. Notes about line marked with #1
2. These items explain why each marked line is important and why this method was chosen

.

 
####<a name=alternatives>Alternative patterns</a>
>#####Ex: Using an if/else block instead of .get method
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
>Other: 
>    Other notes about why a student might have chosen this method and it's effects

 .


>#####Another alternative pattern
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
1. Suggestions to further a student's exploration of the exercise
>`ideal solution for exercise extension`

2. punctuation before counting (some people found string.punctuation or regular expressions)
>`lower_text = re.sub('[!_.,?""''\];:\'\-\()--]', ' ', lower_text)` 

3. etc
>`etc`

