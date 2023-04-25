# Project Team-C

## Introduction 

### Task 1:
Create new issues for each tasks and put labels for them.

### Task 2:
Name the project board, set up workflows for pull requests and issues, add the issues to "To-do", remind groupmates to tag the pull request under task2 project and add "hello" card.

### Task 3:
Set up **`readme.md`** with "Intro", "Code" and "Contributors" in a well-formatted template.

## Task 4:
Implement a C code in code.c, set up a GitHub Action

## Task 5:
Put the C code from Task 4 to **`readme.md`**, hightlight the code with markdown, get a workflow status badge and insert the resultant image.

## Task 6:
Use a loop in `_stu`(Jekyll collection `_stu`)to show all the info of groupmates in **`readme.md`**. It is better to test the implementation in another repo owned by yourself.

## Task 7:
Include the last updated time at the bottom of the page, add a link of Team-C repo into the public repo of **`csci3251-2023.github.io`** and request for review from @chuckjee.

## Code 
```c
{% include_relative code.c %}
```
![c workflow](https://github.com/csci3251-2023/project-team-c/actions/workflows/c-cpp.yml/badge.svg)
## Contributors
{% for stu in site.stu %}
- <img src="{{ stu.image }}" width="50" />@{{ stu.user }} ({{ stu.name }})
    - {{ stu.content | markdownify }}
{% endfor %}
