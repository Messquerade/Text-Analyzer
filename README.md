# _Text Analyzer_

#### _This website will take a passage and analyze it from total number of words, use of a certain search word, etc._

#### By _**Anna Clarke**_

## Technologies Used

* _HTML_
* _CSS_
* _JavaScript_
* _jQuery_
* _Bootstrap_

## Description

_This website will accept a passage and optional search word from the user. The site will then display the number of words in the passage, freguency of the search word, the same passage with all instances of the search word in bold. A feature that will display the most frequently used words in the passage is in development._

## Setup/Installation Requirements

* _Clone this repository from Github to your desktop_
* _Navigate to the top of the directory_
* _Open directory in your text editor of choice_

## Known Bugs

* _Frequency of most used words function is a work in progress_

## License

MIT

Copyright (c) 2021 Anna Clarke

## Contact Information

_Anna Clarke: annac.klingberg@gmail.com_

## Specifications

### Describe: wordCounter()

1. Test: "It should return 1 if a passage has just one word."  
Code:  
const text = "hello";  
wordCounter(text);  
Expected Output: 1

2. Test: "It should return 2 if a passage has two words."  
Code:  
const text = "hello there";  
wordCounter(text);  
Expected Output: 2

3. Test: "It should return 0 for an empty string."  
Code: wordCounter("");  
Expected Output: 0

4. Test: "It should return 0 for a string that is only spaces."  
Code: wordCounter("            ");  
Expected Output: 0

5. Test: "It should not count numbers as words."  
Code: wordCounter("hi there 77 19");  
Expected Output: 2

### Describe: numberOfOccurrencesInText()

1. Test: "It should return 0 occurrences of a word for an empty string."  
Code:  
const text = "";  
const word = "red";  
numberOfOccurrencesInText(word, text);  
Expected Output: 0

2. Test: "It should return 1 occurrence of a word when the word and the text are the same."  
Code:  
const text = "red";  
const word = "red";  
numberOfOccurrencesInText(word, text);  
Expected Output: 1

3. Test: "It should return 0 occurrences of a word when the word and the text are different."  
Code:  
const text = "red";  
const word = "blue";  
numberOfOccurrencesInText(word, text);  
Expected Output: 0

4. Test: "It should return the number of occurrences of a word."  
Code:  
const text = "red blue red red red green";  
const word = "red";  
numberOfOccurrencesInText(word, text);  
Expected Output: 4

5. Test: "It should return a word match regardless of case."  
Code:  
const text = "red RED Red green Green GREEN";  
const word = "Red";  
numberOfOccurrencesInText(word, text);  
Expected Output: 3

6. Test: "It should return a word match regardless of punctuation."  
Code:  
const text = "Red! Red. I like red, green, and yellow.";  
const word = "Red";  
numberOfOccurrencesInText(word, text);  
Expected Output: 3

7. Test: "If an empty string is passed in as a word, it should return 0."  
Code:  
const word = "";  
const text = "red RED Red!";  
wordCounter(word, text);  
Expected Output: 0


### Describe: boldPassage()

1. Test: "It should return a non-matching word in a p tag."  
Code:  
const word = "hello";  
const text = "yo";  
boldPassage(word, text);  
Expected Output: "`<p>`yo`</p>`"

2. Test: "It should return a matching word in a b tag."  
Code:  
const word = "hello";  
const text = "hello";  
boldPassage(word, text);  
Expected Output: "`<p><b>`hello`</b></p>`"

3. Test: "It should wrap words that match in `b` tags but not words that don't."  
Code:  
const word = "hello";  
const text = "hello there";  
boldPassage(word, text);  
Expected Output: "`<p><b>`hello`</b>` there`</p>`"

### Describe: mostFrequentWords():

1. Test: "It should return "" for an empty text  
Code:  
const text = " "  
mostFrequentWords(text);  
Expected Output: ""

2. Test: "It should return "No repeated words" for a string with no repeated words  
Code:  
const text = "The dog hates fleas"  
mostFrequentWords(text);  
Expected Output: "No repeated words"