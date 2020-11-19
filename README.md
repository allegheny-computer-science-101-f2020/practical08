# practical08-solution

## DUE: November 23 by 9:10am

[![Actions Status](../../workflows/build/badge.svg)](../../actions)

## Table of Contents

- [Objectives](#objectives)
- [Introduction](#introduction)
- [Continuous Learning](#continuous-learning)
- [Program Requirements](#program-requirements)
- [Expected Program Output](#expected-program-output)

- [System Commands](#system-commands)

  - [Using Docker](#using-docker)
  - [Using Gradle](#using-gradle)

- [Using GitHub Actions CI](#using-github-actions-ci)

- [Receiving Assistance](#receiving-assistance)

- [Practical Assessment](#practical-assessment)

## Objectives

This assignment invites you to study the source code of a program that is inspired by one outlined in Chapter 10 of the textbook. Specifically, you will study the source code and output of the `WordCount` program that combines the use of the `Tree` and `HashMap` data structures. You will add comments to the source code that clearly explain how the provided program works. Interested students are also invited to add advanced features to this program that, for instance, display the word with the maximum appearance count or support the analysis of multiple input files.

## Introduction

This assignment requires a programmer to understand the methods in a `WordCount` program that is inspired by the source code segment in Section 10.1.2 of the textbook. With that said, the provided source code combines the `Tree` and `HashMap` data structures to implement a more comprehensive solution. Your job for this assignment is to complete and run the program and study its output. Then, you are responsible for adding comments to the source code that demonstrate you understand how the `WordCount` program uses both a `Tree` and a `HashMap` to produce the expected output. Students who are interested in doing so are encouraged to write extra Java methods that can, for instance, print out the word that is most frequently found in the input file. Additionally, you are invited to run the `WordCount` program with a different input file. Finally, as verified by [Checkstyle](https://github.com/checkstyle/checkstyle), the source code for all of the Java classes must adhere to all of the requirements in the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html). The source code in the submitted Java source code files must also pass additional tests set by the [GatorGrader tool](https://github.com/gkapfham/gatorgrader).

## Continuous Learning

If you have not done so already, please read all of the relevant [GitHub Guides](https://guides.github.com/) that explain how to use many of the features that GitHub provides. In particular, please make sure that you have read the following GitHub guides: [Mastering Markdown](https://guides.github.com/features/mastering-markdown/), [Hello World](https://guides.github.com/activities/hello-world/), and [Documenting Your Projects on GitHub](https://guides.github.com/features/wikis/). Each of these guides will help you to understand how to use both [GitHub](http://github.com) and [GitHub Classroom](https://classroom.github.com/).

Students who want to learn more about how to use [Docker](https://www.docker.com) should review the [Docker Documentation](https://docs.docker.com/). Students are also encouraged to review the documentation for their text editor, which is available for text editors like [Atom](https://atom.io/docs) and [VS Code](https://code.visualstudio.com/docs). You should also review the [Git documentation](https://git-scm.com/doc) to learn more about how to use the Git command-line client. In addition to talking with the instructor and technical leader for your course, students are encouraged to search [StackOverflow](https://stackoverflow.com/) for answers to their technical questions.

To do well on this assignment, you should also read Section 1.5.2 to learn more about iteration constructs. You should further review Sections 4.1 to 4.3, focusing on the content that explains the steps of both an analytical and an empirical evaluation of an algorithm. Please read all of the content and study all of the technical diagrams and source code segments in Section 3.2\. Finally, please see the course instructor or one of the student technical leaders if you have questions about any of these reading assignments.

## Program Requirements

This practical assignment invites you to complete and understand the implementation of `WordCount` that can produces the output given in the GitHub repository. Specifically, the `WordCount.java` file provides an implementation of the program that effectively combines `Tree` and `HashMap` data structures.

For this assignment, you are invited to study, understand, complete implementation and add comments to this program's source code. You are also required to provide and use a different textual input, stored in `new_sentences.txt`, than what is provided by the instructor. Please make sure that you can write comments that explain how this program uses the combination of a `Tree` and a `HashMap` to output word counts for the paragraph in a provided file. You should also add the required source code so that the program produces the expected output.

Don't forget to run the program and paste its output at the bottom of the file! You should also observe that the code uses the `java.util.TreeMap` -- how would the program's output change if you replace that with a `java.util.HashMap` instead? Try it! Finally, make sure that you can explain this program output, noting how it illustrates the use of a `HashMap`. Please see the course instructor with your questions about this program!

## Expected Program Output

Typing the command `gradle run` in the Docker container produces the following output for the instructor's version of this assignment. The output produced by your program will be different since you are to use different textual input.

```
Reading and tracking the words in the file ...
... Finished reading and tracking the words in the file.

Analysis of the words in the file ...

(key, value) pairs sorted by key:

{a=4, already=1, append=1, associated=3, associates=1, be=1, combining=1, create=1, either=1, example=1, for=2, function=1, given=2, if=2, is=3, it=1, key=2, mapped=1, mapping=1, may=1, method=1, msg=1, multiple=1, non=1, not=1, null=3, of=2, or=3, otherwise=1, remapping=1, removes=1, replaces=1, result=1, results=1, specified=1, string=1, the=6, this=1, to=2, use=1, value=4, values=1, when=1, with=4}

(key, value) pairs sorted by value and key:

[already=1, append=1, associates=1, be=1, combining=1, create=1, either=1, example=1, function=1, it=1, mapped=1, mapping=1, may=1, method=1, msg=1, multiple=1, non=1, not=1, otherwise=1, remapping=1, removes=1, replaces=1, result=1, results=1, specified=1, string=1, this=1, use=1, values=1, when=1, for=2, given=2, if=2, key=2, of=2, to=2, associated=3, is=3, null=3, or=3, a=4, value=4, with=4, the=6]

... Finished the analysis of the words in the file.
```

## System Commands

This project invites students to enter system commands into a terminal window. This assignment uses [Docker](https://www.docker.com) to deliver programs, such as `gradle` and the source code and packages needed to run [GatorGrader](https://github.com/GatorEducator/gatorgrader), to a students' computer, thereby eliminating the need for a programmer to install them on their development workstation. Individuals who do not want to install Docker can optionally install of the programs mentioned in the [Program Requirements](#program-requirements) section of this document.

### Using Docker

Once you have installed [Docker Desktop](https://www.docker.com/products/docker-desktop), you can use the following `docker run` command to start `gradle grade` as a containerized application, using the [DockaGator](https://github.com/GatorEducator/dockagator) Docker image available on [DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

The aforementioned command will use `"$(pwd)"` (i.e., the current directory) as the project directory and `"$HOME/.dockagator"` as the cached GatorGrader directory. Please note that both of these directories must exist, although only the project directory must contain something. Generally, the project directory should contain the source code and technical writing of this assignment, as provided to a student through GitHub. Additionally, the cache directory should not contain anything other than directories and programs created by DockaGator, thus ensuring that they are not otherwise overwritten during the completion of the assignment. To ensure that the previous command will work correctly, you should create the cache directory by running the command `mkdir $HOME/.dockagator`.

If you are running your program on a Windows Operating System, you should run the following command instead, replacing the word "user" with the username of your machine:

```bash
docker run --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator
```

Here are some additional commands that you may need to run when using Docker:

- `docker info`: display information about how Docker runs on your workstation
- `docker images`: show the Docker images installed on your workstation
- `docker container list`: list the active images running on your workstation
- `docker system prune`: remove many types of "dangling" components from your workstation
- `docker image prune`: remove all "dangling" docker images from your workstation
- `docker container prune`: remove all stopped docker containers from your workstation
- `docker rmi $(docker images -q) --force`: remove all docker images from your workstation

### Using Gradle

Since the above `docker run` command uses a Docker image that, by default, runs `gradle grade` and then exits the Docker container, you may want to instead run the following command so that you enter an "interactive terminal" that will allow you to repeatedly run commands within the Docker container.

In Linux and Mac OS:

```bash
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

In Windows OS:

```bash
docker run -it --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator /bin/bash
```

Once you have typed this command, you can use the [GatorGrader tool](https://github.com/GatorEducator/gatorgrader) in the Docker container by typing the command `gradle grade` in your terminal. Running this command will produce a lot of output that you should carefully inspect. If GatorGrader's output shows that there are no mistakes in the assignment, then your source code and writing are passing all of the automated baseline checks. However, if the output indicates that there are mistakes, then you will need to understand what they are and then try to fix them.

You can also complete several important Java programming tasks by using the `gradle` tool. For instance, you can compile (i.e., create bytecode from the program's source code if it is correct) the program using the command `gradle build`. Here are some other commands that you can type:

- `gradle grade`: run the [GatorGrader](https://github.com/GatorEducator/gatorgrader) tool to check your work
- `gradle clean`: clean the project of all the derived files
- `gradle check`: check the quality of the code using Checkstyle
- `gradle build`: create the bytecode from the Java source code
- `gradle run`: run the Java program in the command-line
- `gradle cleanTest`: clean the JUnit test suite of derived files
- `gradle test`: run the JUnit test suite and display the results
- `gradle tasks`: display details about the Gradle system

To run one of these commands, you must be in the main (i.e., "home base") directory for this assignment where the `build.gradle` file is located.

## Using GitHub Actions CI

This assignment uses [GitHub Actions CI](https://github.com/features/actions) to automatically run [GatorGrader](https://github.com/GatorEducator/gatorgrader) and additional checking programs every time you commit to your GitHub repository. The checking will start as soon as you have accepted the assignment -- thus creating your own private repository. If you do not see either a yellow ● or a green ✔ or a red ✗ in your listing of commits, then please contact the instructor.

## Receiving Assistance

If you are having trouble completing any part of this project, then please talk with either the course instructor or a student technical leader during the course session. Alternatively, you may ask questions in the Slack workspace for this course. Finally, you can schedule a meeting during the course instructor's office hours.

## Practical Assessment

The grade that a student receives on this practical assignment is a checkmark grade (0 or 1) and is based on:

- **Percentage of Correct Gatorgrader Checks**: Students will receive 1 if their solution passes at least 85% (24/28) of GatorGrader checks, otherwise they will receive 0\. Students are encouraged to repeatedly revise their source code in an attempt to get their GitHub Actions CI build to pass.
