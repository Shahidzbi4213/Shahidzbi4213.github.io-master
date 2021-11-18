---
layout: project
type: project
published: false
image: images/debt.png
title: Secure Debt Tracker
permalink: projects/debt
date: 2014
labels:
  - C++
  - Secure Coding
  - MySQL
summary: A secure debt tracker standalone application created by four undergraduate CS students for a secure coding class.
---

<img class="ui medium right floated rounded image" src="{{ site.baseurl }}/images/debt.png">

The secure debt tracker is a simple program that was created by three undergraduate students in a ICS491 (a cyber-security class). It has a front-end text UI in C with data stored in a back-end MySQL database.  It keeps track of debts owed between accounts. For instance, if A owes B money, either A or B can create that debt in the database, and then when it’s paid, B can close it.  The C front-end prompts a user to enter in login credentials, then once the user has access they have a limited selection of actions such as checking and adding debts to their account.

All commands and processing take place within the C text-based front-end, with the front-end having options for prompt-style usage (for users) as well as command-line invocation by arguments (hooks into the exact same code as the prompt interface; intended for use by the exploit-demonstration programs). The front-end parses user input and constructs SQL queries from the input, which are then fed into the database. The results are returned and displayed through the C front-end. The MySQL database is hosted on a remote server (fully controlled by the group) so that testers won’t need to construct a full SQL stack on their machines to run the program.

The main focus of this project was to demonstrate the exploitation of potential security flaws in our program and provide secure code that fixes these problems. By completing this project, I learned how much work goes into securing even the simplest of programs. We found numerous security flaws in our “unsecured” version such as susceptibility to buffer overflow, tainted data and number handling, and data (SQL) injection. I gained skills in working with databases (prior to this, my experience was very limited), using SQL embedded in C code, and in catching security flaws.


You can view the full documentation [here](https://docs.google.com/document/d/1ILk1Cq3Ova6Zs8JeybHzSAPk6YtrcbDQovbuT-jWKSY/edit?usp=sharing).
You can view the source code [here](https://code.google.com/p/ics491a3/).
