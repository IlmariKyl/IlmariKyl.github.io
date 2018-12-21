---
layout: default
---


## Introduction

This page contains a brief "documentation" of what we have done and what I have learned during the Command-line Course arranged in fall 2018.
The main focus on the course was on learning how to use the Unix command-line, but many other useful tricks and tools were also introduced along the way.


![likehome][id1]

[id1]: http://edinburgh-creative-media.s3-eu-west-1.amazonaws.com/assets/basic-terminal-commands-that-you-should-know.jpg "No place like ~/"

<br/> 
The weekly schedule of the course was as follows:

| Week          | Topics                                    |
| ------------- |:-----------------------------------------:|
| Week 1        | Introduction to Command-Line Environments |
| Week 2        | Navigating a UNIX System                  |
| Week 3        | Corpus Processing                         |
| Week 4        | Scripting and UNIX Configuration Files    |
| Week 5        | Installing and Running Programs           |
| Week 6        | Version Control                           |
| Week 7        | Building Webpages using GitHub Pages      |		

<br/>

## Week 1

**Main topics:** *installing, launching and quitting terminal, file formats & some basic commands*

As I had already installed Ubuntu Virtual machine on my computer and I knew the very basic UNIX commands, I didn't learn that much new things during the first week. However, getting more familiar with the `wget` command turned out to be very useful, I don't think there is an equivalent for that in Windows.  

* `wget [option] [URL]` *Retrieves content from web servers*

## Week 2

**Main topics:** *Navigating in the filesystem, user and permission control, processes & remote servers*

Maybe the most useful things for me this week were processes and permissions. Running processes/jobs in the background with `&` after the command, checking the status with `jobs`, listing them with `ps` and killing them with `kill PID` were maybe the most interesting commands this week.

## Week 3

**Main topics:** *Commands for processing text files and corpora, stdin/stdout/stderr, Regular expressions*

I think this week the best things for me were the text processing/previewing/searching commands. Some of them are described below:

* `head [options] <file_name>` *Display the beginning of a text file or piped data*  
* `tail [options] <filename>` *Display the tail end of a text file or piped data*  
* `grep [options] pattern [files]` *Search plain-text data sets for lines that match a regular expression*  
* `sed [options]... {script} <input-file>... ` *Parse and transform text*  

## Week 4

**Main topics:** *Scripting, .bashrc, environment variables*

This week we created a lot of sripts and it was good for practicing the shell scripts syntax as it's a bit different from other programming language syntaxes I'm familiar with.  
<br/>
For example, here's a script that checks whether a file with the given argument as name exists.

```bash
if [ $# -ne 1 ]
then
    echo "ERROR! Wrong amount of command-line arguments."
    echo "Usage: $0 <inputfile>"
    exit 1
fi

IFILE=$1

if [ ! -f "$IFILE" ]
then  
    exit 1 # File doesn't exist
else  
    exit 0 # File exists
```
<br/>
I also found creating aliases and customizing the prompt in ``.bashrc`` to be very useful.

## Week 5

**Main topics:** *Installing programs, Makefile, package managers*

This week I learned some useful, more specific information about installing programs, e.g. the default installing locations and how to use Makefile. Makefile was a completely new thing to me, but it will surely be useful in the future.  
<br/>
Its syntax is basically:

```bash
targets: prerequisites
	recipe
	...        
```

<br/>
A simple Makefile could look like this:
```bash
mytarget: myfile.sh
	# copy myfile.sh to mytarget
	cp -f myfile.sh mytarget
```

## Week 6

**Main topics:** *Git, GitHub*

I was already somewhat familiar with Git and GitHub, but as I don't use them regularly it was very good to study them again.

![git][id2]

[id2]: https://zeroturnaround.com/wp-content/uploads/2016/02/GitHub-cheat-sheet-graphic-v1.jpg "Git cheat sheet"

Especially revising how to work with branches was useful for me.

## Week 7

**Main topics:** *Installing and using Jekyll & creating your own GitHub Pages site*

This website was build as the final project on the course using Github Pages. Designing you own website with these tools turned out to be quite fun and easy. The markdown syntax is very simple and inserting different elements (images, tables, code blocks) is really straightforward.
