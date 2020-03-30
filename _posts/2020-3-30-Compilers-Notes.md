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

### Lecture 1: March 30, 2020

##### Question 1: What is the structure of a Compiler? 

Answer: Conceptually, a compiler can has a front end and a back end. The front end take in source code and compiles it into an intermediate representation. Then, the back-end translates it into target code for machines to read and execute.

##### Question 2: What does the front end consist of? 

Answer: The front end consists of the Scanner, Parser, and also performs Semantic Analysis. 

##### Question 3: What does the back end consist of? 

Answer: The back end consists of target code generation and optimization.

##### Question 4: What does the Scanner do?

Answer: The scanner parses source code and tokenizes the necessary code. It creates a token stream. 

##### Question 5: What does the Parser do? 

Answer: The parser takes the token stream and creates a Intermediate Representatins (IR). This is usually an Abstract Syntax Tree (AST).

