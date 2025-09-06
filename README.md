# ECE2112_ACPA_MUSONG_FOLDER
Advanced Computer Programming and Algorithm_MUSONG

This project contains three beginner Python programs that help practice working with strings, lists, and dictionaries.


# 1. Alphabet Soup Problem

Purpose:
Arrange the letters of a given word in alphabetical order.

Code Used:

```
def alphabet_soup(word):
    return ''.join(sorted(word))   # sorts letters alphabetically

user_input = input("Enter a word (e.g. 'hacker'): ")
result = alphabet_soup(user_input)
print("Alphabetically sorted word:", result)
```

# How it Works:

```` sorted(word)````

Takes the word and splits it into individual letters.

Then it rearranges those letters in alphabetical order.
Example:
"hello" → ['e', 'h', 'l', 'l', 'o'].

```` ''.join(...)````

The join function glues a list of characters back together into one word.

The '' means “don’t put anything between the letters.”
Example:
['e', 'h', 'l', 'l', 'o'] → "ehllo".


Example Run:

Enter a word (e.g. 'hacker'): hacker  
Alphabetically sorted word: acehkr


# 2. Emoticon Problem

Purpose:
Replace certain words in a sentence with emojis/emoticons.

Code Used:
```
def sentence(emote):
    emoticons = {"smile": ":)", "grin": ":D", "sad": ":(", "mad": ">:("}
    Emote_list = emote.split()   # breaks sentence into words
    converted = [emoticons.get(e, e) for e in Emote_list] 
    return ' '.join(converted)

user_input = input("Enter a sentence (e.g. 'Make me smile'): ")
output = sentence(user_input)
print(output)
```

# How it Works:

```` emote.split() ````

Cuts a sentence into pieces (words) wherever there are spaces.
Example: "smile sad" → ["smile", "sad"].

```` emoticons.get(e, e) ````

Looks at each word.

If the word is in the emoticons dictionary (like "smile": ":)"), it replaces it with the matching emoji.

If the word isn’t in the dictionary, it just keeps the word as it is.

```` ' '.join(...)````

Glues all the words (or emojis) back together into a single sentence, with spaces in between.
Example: [":)", ":("] → ":) :(".


Example Run:

Enter a sentence (e.g. 'Make me smile'): Make me smile  
Make me :)



# 3. Unpacking List Problem

Purpose:
Split a list of numbers into first, middle, and last values.

Code Used:
```
user_input = input("Enter a list of numbers separated by spaces (e.g. '1 2 3 4 5 6'): ")
lst = [int(x) for x in user_input.split()]   # convert input into numbers

if len(lst) >= 3:
    first, *middle, last = lst   # unpacking
    print("first:", first, "middle:", middle, "last:", last)
else:
    print("Please enter at least 3 numbers.")
```

# How it Works:

```` input().split() ````

split() cuts it into a list of text pieces (strings):
["10", "20", "30", "40", "50"].

```` [int(x) for x in ...] ````

This turns each text number into a real integer.

So now it becomes:
[10, 20, 30, 40, 50].

```` first, *middle, last = lst ````

This is called unpacking.

first gets the very first number → 10.

last gets the very last number → 50.

*middle takes everything in between → [20, 30, 40].


Example Run:

Enter a list of numbers separated by spaces (e.g. '1 2 3 4 5 6'): 1 2 3 4 5 6  
first: 1 middle: [2, 3, 4, 5] last: 6
