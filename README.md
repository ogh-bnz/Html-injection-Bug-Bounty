



## Unter Writting 





# Html-injection-Bug-Bounty-
## Overview
This repository is a collection of in-depth articles documenting the bug hunting journey within our codebase. Each article is dedicated to a specific bug, issue, or vulnerability that has been identified and resolved during the development process. [ BTW: i just used chatgpt, gemini advance and own things to write this article full filly and make it easy to read .. ]

# Topic
![HTML Injection](https://github.com/ogh-bnz/Html-injection-Bug-Bounty-/assets/99647279/a1b631b3-6947-459a-afe8-24d182060db0)

# Lets talk about `HTML Injection`
--- --- --- --- --- --- --- --- ---
Hello, Our let's understanding HTML injection vulnerability.

At the outset we have not corrected all our confusions and misconceptions

**What is HTML?**
HTML, or Hypertext Markup Language, serves as the foundation for building webpages. Through HTML, you can specify the placement of paragraphs, user input areas, and more on a webpage. Virtually all websites utilize HTML, making it susceptible to HTML injection.

**What is HTML Injection?**
HTML Injection is a vulnerability similar to cross-site scripting. In the case of cross-site scripting, attackers inject JavaScript code and execute it if the target is vulnerable. With HTML injection, attackers can inject certain HTML tags, though not all.

Let's take a practical look at this vulnerability.

I'll be using a demo website for testing purposes: http://testphp.vulnweb.com/




