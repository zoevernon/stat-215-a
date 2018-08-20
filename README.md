# Repository for submitting labs for STAT 215A Fall 2018

This repository contains a set file structure for submitting the projects.

## Setup

Your report and code will be submitted via GitHub. The following instructions will show you how to set up your GitHub account and configure a repository so that you can submit your assignments. This workflow is shamelessly copied (with slight modifications) from Chris Paciorek and Jarod Millman's setup from when I took their STAT243 class way back in 2014.

1. Install Git on your system (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

1. Sign up for GitHub (https://github.com/).

1. Go to https://education.github.com/ and sign up for the student pack to get unlimited private repositories. You are a "student" and you want an "individual account".

Once you have completed these first steps, you are then ready to create your private GitHub repository for this class.

1. Locally on your machine, clone my stat215a repository: `git clone https://github.com/zoevernon/stat215a. This will create a copy of the repository on your own computer.

1. On the GitHub website, log in and create a **private** remote repository called *stat215a*. Add me (*zoevernon*) as a collaborator for this repository (check out settings on the repo website).

1. Back in the terminal, set the origin of your local repository to be the remote repository that you just made. Change USERNAME below to your username. This tells git which remote repository to push your changes to when you `git push` (`git remote set-url origin https://github.com/USERNAME/stat215a.git`).

1. Edit *info.txt* to reflect your own information.

```
name = "Jane Smith"
SID = "0123456789"
email = "jsmith@berkeley.edu"
github_name = "janesmith"
```

Now you're ready to push to your remote repository for the first time:

1. Check git status `git status`. You should see a bunch of text including `modified:   info.txt`.

1. Add (`git add info.txt`) and commit (`git commit -m “Updated info.txt with my own information”`) your edited *info.txt* file

1. Push your changes to your copy of the remote repository (`git push` or sometimes `git push remote origin`)

1. Check that info.txt has been updated in your remote github repository by navigating to https://github.com/USERNAME/stat215a (change USERNAME to your username)

## Submitting your projects

To submit your projects, you will need to create a subfolder in your local `stat215a` folder called `lab1` (if you are submitting lab 1). Inside this folder you should have the following (exact) structure:

```
lab1/
  homework.pdf
  lab1.Rmd
  lab1.pdf
  lab1_blind.Rmd
  lab1_blind.pdf
  R/
  extra/
```

- The source of your report (with code) will be contained in the `lab1.Rmd` file (`lab1.Rnw` is fine too).

- The compiled version of your report will be contained in `lab1.pdf`.

- You will also submit a "blind" version of each of these documents that does not include your name (`lab1_blind.Rmd` and `lab1_blind.pdf`).

- The `R/` folder will contain any extra R scripts needed to compile your report.

- The `homework.pdf` file will contain your completed homework. Please do not include any irrelevant files.

Note that GitHub cannot host files more than 100 MB. If you try to push a file larger than this, GitHub will cry. This means you should avoid pushing the data to your GitHub.  

When you are ready, you need to add, commit, and push the `lab1/` folder.

At the time when the lab is due, we will run a script that automatically pulls all of your assignments into my local versions of your `stat215a` repositories. Please make sure to submit your labs on time. We will spend some time in a lab having everyone submit a pretend assignment so that you are all clear on what to do.

Note: this document was originally written by Rebecca Barter in Fall 2017 and edited to reflect the changes in the course.  