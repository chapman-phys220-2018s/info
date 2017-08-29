# Getting Started Guide

## Introduction

There is a lot of material covered at the beginning of this course that may seem unfamiliar, or scary. In the sage words of Douglas Adams, **Don't panic.**

<img src="https://octodex.github.com/images/femalecodertocat.png" width="25%" />

The aim of this course is to introduce you to industry-standard tools and practices, so that you will be prepared to deliver professional-grade work to colleagues. 
Much like reading and writing, computer literacy is becoming indispensible. 
Easily solved problems are largely solved already. 
The challenging problems that still remain are often too complex for traditional analytical methods to make substantial progress. 
Computational methods help augment other problem-solving methods and increase their effective scope; as a result, they have become increasingly necessary for progress. 
The rise in popularity of "Data Science" and "Big Data" is a symptom of this trend: Computational power enables novel problem solutions.

Being familiar with modern computational tools and techniques will give you an edge in the job market, and make transitioning out of college to the next chapter of your life more smooth. The material of the course may seem daunting---perhaps even overwhelming---at first, but rest assured that practice makes perfect. What is initially unfamiliar and strange will become second nature by the end of the course, and you will have gained a powerful set of new skills that can continue to evolve with the rapid pace of technology. Be patient with yourself, for polishing these new skills will only help you to be a valuable and competitive colleague in the future.

## Account Setup

Our class will be centered around three cloud-based pieces of technology: 
 1. [CoCalc](https://cocalc.org), a linux server in the cloud with free software installed for you to use.
 1. [GitHub](https://github.com), a central hub for sharing code that has become standard in the open-source community. 
As such, you will need to make accounts in both places and make them communicate to each other.
 1. [Slack](https://scststudents.slack.com), a professional communication platform now standard in industry.

 - **Task 1:** Use your Chapman email to create a GitHub account, a CoCalc account, and a Slack account. Use your full, real name when making the accounts so that you can be easily found. The instructor will invite you to the course GitHub Organization, the CoCalc course, and the Slack organization using your student email, so look for the invite emails.
 - **Task 2:** (Optional) If you like, you can link your CoCalc account to your GitHub to simplify logging in. In your CoCalc account, go to the Settings tab at the top of the screen (with the gear icon), and click on the GitHub logo (the *octocat* mascot logo :octocat:).
 - **Task 3:** Join the `#phys220-2017f` channel for the course in Slack. Note that there are a variety of other Slack channels of potential interest, such as `#physics` or `#math` or `#cpsc` or `#jobopportunities` or `#gamedev` or `#chapman-robotics`, etc.
 
## CoCalc Project Setup

If all is well, you should see a course **project** in your main CoCalc window. Clicking on it will log into an *Ubuntu Linux* cloud computer that will run your class project. When your accounts and projects have all been created successfully, the instructor will add *internet access* to each one manually. Prior to this step, your project will be able to create files and run code normally, but will not be able to connect to external websites such as GitHub.

The interface for navigating folders, creating, and editing files is relatively self-explanatory. Questions can be handled in class, if the Help documentation does not already answer your question.

## Setting up the Linux Terminal (a.k.a. Bash Shell) and SSH

After you verify that your project has internet access (you can check the project Settings tab), we can connect to GitHub via **s**ecure **sh**ell keys (ssh keys). To do this, first open a Linux Terminal. CoCalc has the odd feature of creating a new file for each terminal instance, so it is recommended to create a primary terminal in the main directory of your project that you will use. To do this, type the word "terminal" in the search box (upper left corner of the Files tab of your project). It should report "No files found" and show a panel of possible file types you want to create with that name. Choose the button ">_ Terminal" to create a new Linux Terminal running the Bash Shell.  It should look something like this:

```
                ┌────────────────────────────────────────────┐
┌───────────────┤ Welcome to the CoCalc Terminal Environment ├─────────────────┐
│               └────────────────────────────────────────────┘                 │
│ Software: sage R ipython gap gp git latexmk isympy java julia octave python3 │
│ vim emacs nano joe gcc clang ocaml pdflatex xetex node convert mc htop atop …│
│                                                    ┌─────────────────────────┤
│ Anaconda Python [continuum.io]:  anaconda3         │ Usage: type command and │
│                ... and exit it:  exit-anaconda     │ then hit the return key │
│                                                    └─────────────────────────┤
│ Learn about the Linux terminal:     http://ryanstutorials.net/linuxtutorial/ │
│ Experiencing any problems or is something missing?   email help@sagemath.com │
└──────────────────────────────────────────────────────────────────────────────┘
 
~$  
```

This login screen for the terminal gives a nice summary of all the useful software installed in your linux computer in the cloud, and suggests a good tutorial for how to use the bash shell.  (You can also find many more resources in this `info` repository in the course GitHub Organization. For a quick introduction, see the [Linux/Bash Overview Slides](http://slides.com/profdressel/linux-bash-overview).)

To connect to GitHub, we first need to create `ssh` keys for your linux computer. To do this, type the following command into the terminal, and hit `Enter` four times (don't type the *prompt* characters `~$` - this is printed to let you know that you may type something):
```
 ~$ ssh-keygen
```
This will generate keys in the folder `~/.ssh/` that you can add to your GitHub account so that it knows who you are.
