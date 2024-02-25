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

I'll be using a demo website for testing purposes: `http://testphp.vulnweb.com/`

Threat Model:
1. Open Your Target Site -

![image](https://github.com/ogh-bnz/Html-injection-Bug-Bounty/assets/99647279/49a4941c-929b-46a7-a754-b3eadff408f5)

3. Now, enter the specified payload in the search field.

   `<h1 style=”color:Blue;”>TCH Community</h1>`

![image](https://github.com/ogh-bnz/Html-injection-Bug-Bounty/assets/99647279/9813248e-c102-4c5f-b0ed-7bd772d7feec)

3. Now, press the go button, and the 'TCH Community' will change its color to blue  

![image](https://github.com/ogh-bnz/Html-injection-Bug-Bounty/assets/99647279/fddd91ef-4ae5-45c1-a249-857d339ab095)

4. Success! The website Display HTML Injection, indicating vulnerability to this type of attack

# How to identifying this vulnerabilities in websites?

* The methodology of `Html-injection` is:

    1. locating all user input fields and verify if the input provided is echoed/return back on the website
    2. Attempt injecting standard HTML tags, such as heading tags, and observe the website's response.
    3. In case the HTML code is executed, it indicates the presence of an HTML injection vulnerability. It's essential to continue the investigation beyond this point. So Don't Stop Here
    4. Attempt injecting JavaScript code. If the JavaScript code is successfully executed, you have identified an XSS vulnerability.

# Which areas should you explore to identify `HTML-Injection` vulnerabilities ?

* The most effective ways to prevent HTML Injection are:

    1. `Input Validation`: Define strict rules for what data is allowed and reject anything that doesn't fit.
    2. `Output Encoding`: Convert HTML special characters (<, >, &, etc.) into their safe HTML entities (e.g., &lt; for <) before displaying user-supplied data. This prevents the browser from interpreting them as executable code.
    3. Content Security Policy (CSP): A powerful mechanism to help prevent HTML injection, XSS, and other attacks by controlling what code can execute on your site.

* Also you can use this ways for find this vulnerability:
    1. Search Bars
    2. Contact Forms
    3. Comment Sections
    4. User Registration Forms
    5. Login Forms
    6. Feedback Forms
    7. Product Reviews
    8. Chat Boxes
    9. Newsletter Signup
    10. Profile Information, more

# This is the usual way to discover HTML Injection vulnerabilities !

* I hope the article is clear. Before concluding, I'd like to share some write-ups and HackerOne reports that can assist you in identifying HTML injection vulnerabilities.

    1. https://github.com/nextcloud/security-advisories/security/advisories/GHSA-wgpw-qqq2-gwv6 [ GitHub ]
    2. https://hackerone.com/reports/2210038 [ Hackerone ]
    3. https://hackerone.com/reports/358001 [ Hackerone ]
    4. https://medium.com/@pratiky054/html-injection-unique-exploitation-a5c3d4e6fed8 [ Medium ]
    5. https://www.softwaretestinghelp.com/html-injection-tutorial/ [ Software Testing ]




# Thanks, 220
--- --- --- --- --- --- --- --- ---

* Join Telegram Community - https://t.me/tch_community
* Follow on Linkedin - https://www.linkedin.com/in/ogh-bnz/
* Subscribe on YouTube - https://www.youtube.com/@RootMate?sub_confirmation=1
* If you have any qus ? - rhashibur75@gmail.com

# 📝 : Kazi Hashibur Rahman | CheckMate
