# 1. Write a Python NLTK program to split the text sentence/paragraph into a list of words.
```
text = '''
Joe waited for the train. The train was late. 
Mary and Samantha took the bus. 
I looked for Mary and Samantha at the bus station.
'''
print("\nOriginal string:")
print(text)
from nltk.tokenize import sent_tokenize
token_text = sent_tokenize(text)
print("\nSentence-tokenized copy in a list:")
print(token_text)
print("\nRead the list:")
for s in token_text:
    print(s)
    
 ```

# 2. Write a Python NLTK program to tokenize sentences in languages other than English.
```
text = 
'''
NLTK ist Open Source Software. Der Quellcode wird unter den Bedingungen der Apache License Version 2.0 vertrieben.  
Die Dokumentation wird unter den Bedingungen der Creative Commons-Lizenz Namensnennung - Nicht kommerziell - Keine 
abgeleiteten Werke 3.0 in den Vereinigten Staaten verteilt.
'''
print("\nOriginal string:")
print(text)
from nltk.tokenize import sent_tokenize
token_text = sent_tokenize(text, language='german')
print("\nSentence-tokenized copy in a list:")
print(token_text)
print("\nRead the list:")
for s in token_text:
    print(s)
```

# 3. Write a Python NLTK program to create a list of words from a given string.
```
from nltk.tokenize import word_tokenize
text = "Joe waited for the train. The train was late. Mary and Samantha took the bus. I looked for Mary and Samantha at the bus station."
print("\nOriginal string:")
print(text)
print("\nList of words:")
print(word_tokenize(text))

```

# 4. Write a Python NLTK program to split all punctuation into separate tokens.
```
from nltk.tokenize import WordPunctTokenizer
text = "Reset your password if you just can't remember your old one."
print("\nOriginal string:")
print(text)
result = WordPunctTokenizer().tokenize(text)
print("\nSplit all punctuation into separate tokens:")
print(result) 

```


$Run these 4 code snippet and implement them in your assignment notebook$
