---
date: 2019-05-1T20:04:40.407Z
title: Petition Pronto
---
<h4>My Hugo Blog</h4>
During my Spring Semester 2019, I worked with a team to contribute to the
different features that make GatorGrader.

Designed to help check students work and inform of them any errors concerning
their work, the tool employ many command line arguments that provide multiple
checks to ensure you configure the tool with the correct command-line arguments.
The following indicates the different command line arguments GatorGrader uses and
what they do.

<!--more...-->
---

```
usage: gatorgrader.py [-h] [--nowelcome] [--json] [--commits COMMITS]
                      [--directory DIR] [--file FILE] [--exists]
                      [--single COUNT] [--multiple COUNT]
                      [--language {Java,Python}] [--paragraphs COUNT]
                      [--words WORDS] [--command COMMAND] [--executes]
                      [--fragment FRAGMENT] [--count COUNT] [--exact]

optional arguments:
  -h, --help            show this help message and exit
  --nowelcome           do not display the welcome message (default: False)
  --json                print reports in JSON (default: False)
  --commits COMMITS     minimum number of git commits (default: None)
  --directory DIR       directory with file for checking (default: None)
  --file FILE           file for checking (default: None)
  --exists              does a file in a directory exist (default: False)
  --single COUNT        minimum number of single comments (default: None)
  --multiple COUNT      minimum number of multi comments (default: None)
  --language {Java,Python}
                        language for the single comments (default: None)
  --paragraphs COUNT    minimum number of paragraphs (default: None)
  --words WORDS         minimum number of words in paragraphs (default: None)
  --command COMMAND     command to run (default: None)
  --executes            does a command execute without error (default: False)
  --fragment FRAGMENT   fragment that exists in code or output (default: None)
  --count COUNT         how many of an entity should exist (default: None)
  --exact               equals instead of a minimum number (default: False)
```

GatorGrader can be used with other tools to provide supplemental information and
even more checks of source code and technical writing.

During this class I worked on two issues with my fellow team members and one
issue by myself. The first issue I worked on, has functioning code that brings
the feature of checking for issues created, discussed, and then closed. I added
a function that can get a specific issue and gets access from GitHub to print the
specific issue called for by the student. The second aspect of the function is
that it will state whether that issue if closed or open, and if need be the
student can print all of either.

The second issue I worked on is creating a logo for GatorGrader with my fellow
teammate Christian Walker. I helped create the logo and then I detail the project
summary in the README.md.

The final issue that I began working on was checking commit messages for fragments
and/or length. The function that I began working on will check for non-alphanumeric
characters and determine whether the characters are not valid characters. The aim
of this function is to determine students reactions toward fixing an issue
(expressed by emojis) and then capture those emotions.

Link to GitHub repository: https://github.com/GatorEducator/petition-pronto
