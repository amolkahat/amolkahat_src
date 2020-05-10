Title: {"Pythonpune" : Python3-101}
Date: 2016-01-24 19:59
Author: amolkahat
Category: Pythonpune
Tags: python3
Slug: python3_101
Status: published

"PythonPune" organized Python3-101 workshop on 23rd Jan, 2016 at Red Hat, Pune (India) Office. It was a hands-on workshop.

That was another awesome meetup by "PythonPune" meetup group. The meetup was specially about python3 basics.

The speakers in the meetup was **Kushal Das** - CPython Core Developer, Fedora Cloud Engineer, **Praveen Kumar** - Software Engineer and **Sayan Chowdhury** - Fedora Infrastructure Engineer.

At the beginning Praveen introduced speakers to audience and gave intro about meetup.Then Kushal spoke about python and its basic concepts. Like everyone knows that python2 and python3 have lots of differences in modules and some tags.

<!--more-->Consider that in python2 if we divide a number (Say 5/2 which gives 2 )  we get output in integer format. But if we try same thing in python3 ( 5/2 which gives 2.5 ) gives output in float format.

After that Kushal explained about Variables, Operators and Expressions, Control Flows, Functions and Strings. Which was not hard to understand for anyone. Participants in the meetup got good knowledge of python3.

Then Kushal started Data Structure which is my favorite part. Kushal discussed Dictionary and its some python2 methods which are deprecated from python3 (Like python3 don’t have has\_key() method). Next part was list, sets and list comprehension.

Next discussion was on modules, like importing modules create your own modules. Also he explained the use of **\_\_name\_\_** in python.Kushal introduced os, sys, getpass modules. How to use this modules in programs.

The file operations was the best topic in session, opening and closing files using **with** and without **with** was also countable.

During the session Sayan Chowdhury and Kushal gave some programming exercise. Programs like

-   Simple Mathematical Operations
-   If else programs
-   Dictionary Programs
-   Set Programs
-   Factorial
-   FizzBuzz
-   Read Memory file

The "FizzBuzz" is a simple program. The problem was simple, you have to print numbers from 1 to 100. If number divisible by 3 then you have to print "Fizz" if number divisible by 5 then print "Buzz" if no divisible by 3 and 5 then you have to print "FizzBuzz" else print the number as it is. But according to Sayan’s experience, he says 90% of Software Engineer are unable to solve it.

At first look this problem is simple. But main challenge is that solve that problem using list comprehension. So no one solves that problem using list comprehension.

The "FizzBuzz" list comprehension program:

>     x = ['FizzBuzz' if i % 15 == 0 else 'Fizz' if i % 3 == 0 else 'Buzz' if i % 5 == 0 else i for i in range(1, 101)]
>     print(x)

[So finally Kushal introduced us to **IRC**. Which help peoples to solve their problems. [**\#dgplug**](https://dgplug.org/) is a channel where you can ask your query.]

[Thank you ]{style="line-height:1.5;"}[**PythonPune**](https://twitter.com/pythonpune)[ for arranging such beautiful meetup. Thank you [Chandan Kumar](https://twitter.com/ciypro), [Pravin Kumar](https://twitter.com/kumar_pravin), [Sayan Choudhari](#), [Kushal Das.](https://twitter.com/kushaldas)]
