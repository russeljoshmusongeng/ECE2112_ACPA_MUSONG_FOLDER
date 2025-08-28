# ECE2112_ACPA_MUSONG_FOLDER
Advanced Computer Programming and Algorithm_MUSONG

This project contains three beginner Python programs that help practice working with strings, lists, and dictionaries.


1. Alphabet Soup Problem

Purpose:
Arrange the letters of a given word in alphabetical order.

Code Used:

def alphabet_soup(word):
    return ''.join(sorted(word))   # sorts letters alphabetically

user_input = input("Enter a word (e.g. 'hacker'): ")
result = alphabet_soup(user_input)
print("Alphabetically sorted word:", result)

How it Works:

sorted(word) → breaks the word into letters and sorts them alphabetically.

''.join(...) → combines them back into a single string.


Example Run:

Enter a word (e.g. 'hacker'): hacker  
Alphabetically sorted word: acehkr


2. Emoticon Problem

Purpose:
Replace certain words in a sentence with emojis/emoticons.

Code Used:

def sentence(emote):
    emoticons = {"smile": ":)", "grin": ":D", "sad": ":(", "mad": ">:("}
    Emote_list = emote.split()   # breaks sentence into words
    converted = [emoticons.get(e, e) for e in Emote_list] 
    return ' '.join(converted)

user_input = input("Enter a sentence (e.g. 'Make me smile'): ")
output = sentence(user_input)
print(output)

How it Works:

emote.split() → breaks the sentence into words.

emoticons.get(e, e) → replaces the word if it matches one in the dictionary; otherwise keeps it the same.

' '.join(...) → puts the words (or emojis) back into a sentence.


Example Run:

Enter a sentence (e.g. 'Make me smile'): Make me smile  
Make me :)



3. Unpacking List Problem

Purpose:
Split a list of numbers into first, middle, and last values.

Code Used:

user_input = input("Enter a list of numbers separated by spaces (e.g. '1 2 3 4 5 6'): ")
lst = [int(x) for x in user_input.split()]   # convert input into numbers

if len(lst) >= 3:
    first, *middle, last = lst   # unpacking
    print("first:", first, "middle:", middle, "last:", last)
else:
    print("Please enter at least 3 numbers.")

How it Works:

input().split() → turns typed numbers into a list of strings.

[int(x) for x in ...] → converts them into integers.

first, *middle, last = lst → separates the first number, the middle part, and the last number.


Example Run:

Enter a list of numbers separated by spaces (e.g. '1 2 3 4 5 6'): 1 2 3 4 5 6  
first: 1 middle: [2, 3, 4, 5] last: 6
