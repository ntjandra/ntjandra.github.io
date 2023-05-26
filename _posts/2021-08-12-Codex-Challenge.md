---
layout: post
title: Open AI Codex Challenge
date: 2021-08-13 14:30 -0700
tags: code learn me
---

Today I completed the Open AI Codex Challenge! It was super fun and it changed the way I think as a developer. Codex is very hit or miss depending on the number of tasks and the response expectation. Its still a very good coder, having built in understanding of the documentation.

## Problem 1
### Summary
This is the most basic of all data science topics. Given a set of data, find the lifetime (in days) of the table data. There was a roadblock with internet issues and the Open AI server. Codex was down so I was brushing up on the pandas documentation or syntax (Haven't touched it in a year). Then I broke down the problem into subproblems, following an iterative approach of printing logs to console to check.

### Original: 
Given the contents of a CSV file as csv_contents, return the difference in days between the date of the earliest and the oldest entry.

### Approach
1. Convert the dataset into a pandas dataframe
2. Get the Date Column of the dataset
3. Find the first and last values of the date column
4. Calculate the difference in the last and first
5. Convert to number of days and return it.

## Problem 2: 
### Summary
Problem two had me explore an entirely new library, Differ. The goal was to find out what type of changes needed to be done in order to change one input into another input and count the insertions and deletions necessary. Codex was working but with some latency (about 10-15 mins to process), I lost a lot of time running it, and the worse part was that it was my fault. I had given it far too complex instructions and/or too many instructions. During this time I left to get some fresh air and eat lunch then come back to solve it. I decided to try to solve it myself, I read through a lot of the documentation and found a function called ndiff, which returns how two strings vary, then edited it for the '\n' delimiter.

### Problem Statement:
`source` and `target` are two strings each containing file contents. Return the number of lines you would need to insert and the number of lines you would need to delete to get to target from source.

### Approach
1. Parse inputs
2. Extract diff output
3. Parse output symbol
4. Add accordingly to symbol, + v.s -
5. Return count of symbols

## Problem 3:
### Summary
Problem Three was your everyday Leetcode question, about tree data structures. I've done a lot of work regarding prefix trees so I knew what to tell codex in order to solve it. I assumed it knew what leafs were, so I wrote "Once you reach a leaf of the tree ... [do something]". In this case it would be the cross refference with decode tree and append the corresponding value to the result. 

### Problem Statement:
Given a compressed message `compressed` and the prefix code tree used to encode it, decode and return the original message.

### Approach
1. Explore all paths of the prefix tree until reaching a leaf
2. Add leaf to result, and reset original tree
3. Repeat until original input is terminated

## Problem 4
### Summary
When I read Problem four, I knew it was going to take a while if I had to code it from scratch. By this time, Codex was working again and I attempted to solve it by being very clear in my codex instruction. I was amazed by the code it generated and it brought back memories of the Haskell and RISC-V projects back in university. This time, I told it "Get a list of all paths for an import as an abstract syntax tree."
The output was incredible. It used the ast library and imports I've never seen nor heard of (I have a background in research on File I/O and have written packages to perform File I/O).
I ran a few tests to comfirm the output, then I hit submit and it worked. 

### Problem Statement:
Parse the given Python source code and return the list of full-qualified paths for all imported symbols, sorted in ascending lexicographic order.

### Approach
1. Condense problem down into simple steps
2. Ask Codex
3. Submit

## Problem 5
The problem was yet another thing I've done in the past. I had done a larger scale version of this problem at the Skyhook Internship at CROSS and a common data engineering question. It felt lackluster as the final problem especially after problem 4, as it's just another permuation problem about buckets. I broke down the problem into basic logic and formatted it similar to how a math proof would look to ask Codex. The output was exactly how I would have done it in the past.

### Problem Statement

### Approach
1. Clarify codex to use Permuations, and compare
2. Ask Codex
3. Submit

## Comparison and Results
I finished [#463](https://challenge.openai.com/codex/results/Z29vZ2xlLW9hdXRoMnwxMDUzMDUzMTU4MzU2MDYwOTQzMjg=) which is in the top 500 so I'm getting an Open AI Shirt! I'm really excited for that. To reflect, I compared my solutions with Codex.

### Problem 1
Both results were very similar, but Open AI had a solution using min and max date instead of extracting first and large with indexes after a sort. In terms of performance my solution runs trivialy faster, but uses more memory.

### Problem 2
This was done without Codex so I expected it to be very different. Open AI's solution chose different libraries and implictly returned the tuple, while I chose to explicitly return a tuple. My solution did have some human error due to forgotten dead code I forgot to clean up after my testing and overall tiredness. But an IDE would have picked it up, so its not detrimental. In terms of performance, it depends on the dataset having newlines and whitespace.

### Problem 3
The AI used a for loop, but when I used Codex it chose to do a while loop. These minor details made me wonder why it didn't do a while loop in its solution. Along with this as I look back on the problem, it would fail multiple Leetcodes under TLE, since for large secret messages it would be best to use memoization or tabulation to generate a known words list instead of each character by character. Needless to say, a while with an empty else is poor coding practice when it could have been completed with a for loop. Open AI wins this one.

### Problem 4
Due to my instructions my variables were named to find a tree dynamic, while Open AIs solution used statement instead of nodes. It also contains a difficult to understand concatination versus mine which explains why using an if statement.

### Problem 5
As stated earlier, the AI mimiced my style of coding, but the final solution on OpenAI did not. It used a non friendly form of list comprehenssion, which is nice on one line but more difficult to read. In other words, you need someone to understand the solution first to arrive at that conclusion.

## Epiphany 
It scares me how I felt like I would be out of an occupation, but it gave me the drive to have a new retrospective on the future of coders. Codex is an efficient coder, but it doesn't optimize. It's a wonderful helper at the very least. When combined with the knowledge of a professional who can design and break down problems it has the potential to evolve a junior or entry level programmer to be at a senior levels by bridging the gap in experience. Most of these questions I could see being asked in a job interview, and just knowing what libraries to use and shortcut methods such as `isinstance` and `itertools.permuation` help a candidate stand out. In the future, I see a programmer's main job as the understanding of the breakdown of goals along with cleaning up someone or something's code by leaving behind clean documentation to share understanding. To put it simply, the programmer is a specialized product manager in the field of logic.