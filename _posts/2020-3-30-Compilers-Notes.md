---
layout: post
title: "CSE 401: Notes For Compilers"
date: 2020-3-30
description: "I think I'll regret writing this"
img: how-to-start.jpg # add image post
fig-caption:
tag: [Computer Science, University of Washington, Compilers, CSE 401]
---

> *"He found it impossible to study conic sections; something in their calm and tantalizing respectability breathing defiantly through Mr.Rooney's fetid parlors disorted their equations into insoluble anagrams."*
> - F. Scott Fitzgerald, *This Side of Paradise*

# Notes for My Compilers Class

A few days ago, I was reading an article about retaining information you read about. I tend to forget a lot of things very easily. In the article (I forget where I read it now), it said concepts are easier to remember when you take notes in a question-answer format. Instead of writing down just bullet point notes, converting them to questions and answers would help you remember the concepts better. Unfortunately, I don't have the time to think up of questions AND answers during a lecture, so I decided to spend 30 minutes of my time after class to simply convert my bullet point notes into questions + answers. Let's hope this works.

--- 

<details>
<summary>
Lecture 1: March 30, 2020
</summary>

#### Question 1: What is the structure of a Compiler? 
- Answer: Conceptually, a compiler has a front end and a back end. The front end take in source code and compiles it into an intermediate representation. Then, the back-end translates it into target code for machines to read and execute.

#### Question 2: What does the front end consist of? 
- Answer: The front end consists of the Scanner, Parser, and also performs Semantic Analysis. 

#### Question 3: What does the back end consist of? 
- Answer: The back end consists of target code generation and optimization.

#### Question 4: What does the Scanner do?
- Answer: The scanner parses source code and tokenizes the necessary code. It creates a token stream. 

#### Question 5: What does the Parser do? 
- Answer: The parser takes the token stream and creates a Intermediate Representations (IR). This is usually an Abstract Syntax Tree (AST).

</details>

---

<details>
<summary>
Textbook Reading: Chapters 1 & 2.1-2.3
</summary>

#### Question 1: What do you call a compiler that output other programming languages? 
- source-to-source compilers


#### Question 2: What is the Kleene closure?

- the union of concatenations of a regular expression R with itself, zero or more times.

#### Question 3: What operator (^) is this? How about epislon?

- the complement operator
- eplison is the empty string 

#### Question 4: How are non-deterministic automaton different from deterministic automaton?

- An NFA allows transitions on the empty string, and states that have multiple transitions on the same character

</details>

---

<details>
<summary>
Lecture 2: April 1st, 2020
</summary>

#### Question 1: What is the Principle of Longest Match?

- scanner picks the longest possible string to make up the next token if there is a choice. For example, the word "iffy" will be interpreted as "iffy" instead of "if fy", even though there is an "if" keyword in the string.

#### Question 2: What is an automaton?

- a recognizer of a language. It validates a string by confirming or rejecting a string as part of a language. 

#### Question 3: What is a Grammar?

- A generator; a system for producing all strings in the language.

#### Question 4: What is a Production?

- rules of a grammar

</details>

<details>
<summary>
Lecture 3/4: April 3rd and 6th, 2020
</summary>

#### When converting characters into tokens, how do scanners differentiate between similar tokens (ex: != vs !True)?

- At the conceptual level, you can think of your scanner almost "peeking" one character ahead. Since there's no way to tell if ! implies the neq symbol or a negation, the scanner has to look one ahead.

#### How do you implement DFAs as code? 

- You can do one of several things, including implementing the DFA by hand (lots of tedious code but fast) and using a tool to generate table driven scanners.  

</details>