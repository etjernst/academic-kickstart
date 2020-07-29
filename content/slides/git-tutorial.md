---
title: Git tutorial, part 1
summary: Intro to `git`
location: Your computer
authors: []
abstract: ""
tags: []
categories: []

##  Talk start and end times.
##    End time can optionally be hidden by prefixing the line with `#`.
# date: "2019-02-05T00:00:00Z"
# date_end: "2030-06-01T15:00:00Z"
# all_day: false

# Schedule page publish date (NOT talk date).
# publishDate: "2017-01-01T00:00:00Z"

# Is this a featured talk? (true/false)
featured: false

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: beige
  highlight_style: dark
  controls: true
  controlsLayout: 'bottom-right'
  progress: true
  hash: true
  transition: none
  ratio: '16:9'

links:
- icon: twitter
  icon_pack: fab
  name: I spend a lot of time on twitter
  url: https://twitter.com/etjernst
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
# - internal-project


---

{{< slide background-image="https://media.giphy.com/media/hrRJ41JB2zlgZiYcCw/giphy.gif" >}}

<h1 style="color:orange">Don't be like this silly baboon...</h1>

<br>
<br>
<br>

<p class="fragment fade-up" style="color:orange" >
	...use <code>  git </code> !
</p>

</section>

---

<section id="index" style="text-align:left">

# Index
* [Before you start](#pre-reqs)
  * [Git basics](#git-basics)
  * [Git vocab](#git-vocab)
    * [First time setup](#step-0)
    * [New project setup](#project-setup)
* [Practice: staging and committing](#practice-stage-commit)
* [Basic workflow](#basic-workflow)
* _[Branches](#introducing-branches) (coming soon)_
* [Useful commands](#useful-commands)

</section>

---

<section data-markdown id="pre-recs">

  <script type="text/template">

# Before beginning, you need...

1. A [GitHub](https://github.com) account
  - Can you access the  <!-- .element: class="fragment"  data-fragment-index="1" --> [Tutorials](https://github.com/etjernst/Tutorials) repo?
  - If you are logged in to GitHub but clicking on the link  above :point_up: takes you to a 404 error page, then you're most likely not a contributor yet! <!-- .element: class="fragment"  data-fragment-index="1" -->
2. A git client on your computer
  - If you download git from <!-- .element: class="fragment"  data-fragment-index="2"  --> [here](https://git-scm.com/downloads), you should automatically get `git bash`
  - <!-- .element: class="fragment"  data-fragment-index="2"  -->  I use <code>git bash</code>, but there are many other user interfaces (see options <a href="https://git-scm.com/downloads/guis">here</a>)

3. <!-- .element: class="fragment"  data-fragment-index="3"  --> <i>Optional:</i> read <a href="https://web.stanford.edu/~gentzkow/research/CodeAndData.pdf">Gentzkow & Shapiro (2014)</a>

  </script>
</section>

---

<section id="git-basics" style="text-align:left">

# Git basics - what is this thing?

Git is the most popular version control system
  - a bit like if you cross-bred Dropbox & MS Word's "track changes"
  - git is optimized for many of the things that applied economists
  spend a lot of time on (code)

> Yes, there is a learning curve, but it's worth it!

</section>

---

<section id="git-vs-github" style="text-align:left">

# Git $\neq$ GitHub

<s>Git</s> is a local tool that lives on your computer and
1. uses version control to make collaboration infinitely better
2. allows simultaneous editing _and_ execution of scripts
3. gives detailed comparisons between alternate versions<br>
  ...and allows different versions to co-exist _forever!_
4. greatly facilitates transparent and reproducible research

<s>GitHub</s> is a hosting platform that lives in the cloud
  1. GitHub provides a bunch of services built on top of the Git system
  2. I use the command line for most of my day-to-day work, but some things I find easier to do in GitHub
  3. Comparing two versions of code is clearer to me in the GitHub interface

</section>

---

<section>

# GitHub code comparisons example

{{< slide background-image="/img/README-af451bd5.png" background-position="center 0px bottom  0px"  background-size="80%" >}}

</section>

---

<section id="git-vocab">

# Vocab

Git has a ton of terminology & details; I don't know half of it!
> The beauty is that you don't have to understand how git works to start using it!


That said, some terms are useful... to know what to search for among the many helpful git-related websites

<br>

Click the down arrow for vocab!

---

# <s>Repository</s> (a.k.a. repo)

_= basically a project folder_

<br>

* A repo contains all files associated with a project
  * this can (and should) include associated  documentations
  * repos can have multiple collaborators and can be  public or private

* Your project repo also stores <s>every file's revision history</s> :exploding_head:

  > That's pretty amazing, no?

---


# Ok cool, so how do I get one?

You can get a repo in two main ways:

1. You can <s>clone</s> an existing Git repository from elsewhere
    > This is for you if: you have created a repo already, or are joining a project with an existing repo

2. Take a local directory (folder) that is currently not under version control and turn it into a Git repository
    > This is for you if: you have a project folder that you want to start using version control with

---

# <s>Clone</s>

_= to "download" (kind of)_

<br>

* A <s>clone</s> is a copy of a repo that lives on your computer (instead of somewhere in the cloud)

  > What's the difference betwen **cloning** and **downloading**? <br> When git **clones** a repo:
  > * it creates a full copy of **all versions** of every file & folder for the project
  > * plus  it remembers where you downloaded it from!
* Also, the cloned repo stays connected to the remote repo <br>
(i.e. the one in the cloud)
  * in other words, when you make local changes to your file, git knows where these changes belong

---

# <s>Clone</s>

<br>
<br>

If you download your repo instead of cloning it, you just get
the most recent files on the default branch:
* You don't get any of the magic, which lives in a hidden folder called the .git folder
* You can no longer use git in the downloaded folder

---

# <s>Commit</s>

_= a revision_

<br>

Now we know that a project repo stores every file's revision history
* How do changes make it into the history?
* And how is it different from, say, how this works in Dropbox?

<br>
<br>

Dropbox does have version control, i.e.
you can click on files and see previous versions
* One issue is that you get a new version every single time you  save
* If you click `Ctrl+S` a lot (like I do), you end up with tons of changes

---

# Dropbox versions

<section>
  <div id="left">
  <br>
    <p data-markdown>How many of these are meaningful changes?</p>
	<br>
	<br>
	<br>
    <p data-markdown>How would I figure out a week from now
	which of these changes did anything in particular?</p>

<br>

<p data-markdown> _...let alone a year from now!_ </p>

  </div>

  <div id="right">
  <img src="/img/dropbox.png" width="100%" >
  </div>

</section>

---

# How to commit?

<br>

Back in the bad old days, I used to save many versions of files named things like `YYMMDD_docname_INITIALS.doc`

> A commit keeps track of who made what change and when

When you make a <s>commit</s> to save your work,
git creates a unique ID, a `hash`, that records
  1. what changed from the previous version
  2. a time stamp
  3. the user that made the commit

---

# How to commit?

<br>

Unlike Dropbox's constant "versioning", you have to tell git
1. when to commit
2. what to call the commit

   > This is likely the biggest change from your current workflow

By "what to call the commit," I don't mean a new file name
  * commits should contain a **commit message**: a _brief_ summary of the changes in that commit
  * git is always watching for changes and records everything when you commit

---

# <s>Stage</s>

_= tell git to mark the files that you will include in your next commit_

<br>

Staging is an _intermediate_ step between saving a file locally & creating the commit

I am not 100% sure why this step exists.
  * to make it more confusing, the actual command is `add`, not stage
  * as in, you are _adding_ a file to the staging area

<details>
  <summary>
    If you want my best guess, click here (not necessary)
  </summary>

<small>

My best guess/explanation is the following:
say you are testing out a robustness check.
This requires you to edit several .do files.
So you edit `masterDoFile.do` and add it to the staging   area:
```bash
git add "$projectFolder/masterDoFile.do"
```
Then you make some changes to the estimation code,   `estimationCode.do` and add that to the staging area:

```bash
git add "$projectFolder/analysis/estimationCode.do"
```

You can then commit both files, i.e. add them to the   version history with a useful message:

```bash
git commit -m "Robustness check for Table 3"
```

Logically, you changed both of these files in the process
of running a robustness check but maybe you don't see a   reason to have a different commit for the two files.
So the staging step recording what _files_ you have changed   and the commit

</small>

</details>


---

# <s>Pull</s>

_= syncing changes from the remote (e.g. GitHub) to your local repo_

* When you pull from a repository, you retrieve all
commits from that remote repository and
merge them into the local repository
* You should always do this before you start working

<br>
<br>

# <s>Push</s>

_= send (committed) changes to a remote repo (e.g., on GitHub)_

* If you change something locally, nobody else will have access to those changes until you _push_ them to the remote repo

---

# Summary

Now you know the basic pieces of the git workflow!

<br>

1. <s>Pull</s> from the remote <s>repo</s> (or clone if it's the first time you're working in the repo)
  ```bash
  git pull origin master
  ```

2. Make changes to files, working as you normally would: save changes in your local <s>clone</s> and then  <s>stage</s> the changes

  ```bash
  git add '[fileA]'
  git add '[fileB]'
  ```
3. <s>Commit</s> these local changes to your Git history, adding a logical commit message
  ```bash
  git commit -m "Updated bootstrap routine"
  ```
4. <s>Pull</s> from the remote repo just in case anyone else made changes too
  ```bash
  git pull origin master
  ```
5. <s>Pull</s>  your changes to the remote repo on GitHub
  ```bash
  git push origin master
  ```

</section>

---

<section id="first-time">

# Introduce yourself to git

   > You only have to do this the first time you use git on a given computer

  1. Open up git bash, which should have come with the git installation.
  2. Set your name, which will be attached to your commits
  ```bash
  git config --global user.name "[yournamehere]"
  ```
  3. Set your email (same email that you used to sign up for GitHub)
  ```bash
  git config --global user.email "[youremailhere]"
  ```

---

{{< slide background-image="/img/cd.gif" background-position="right 20px bottom 300px" background-size="40%" >}}

<section>

# New project setup

<div id="left"  data-markdown>
* You only need to do this the first time you work with a project on a given   computer
* You can follow these steps with a public repo,
  or with a private repo to which you've been added as a collaborator

<p>
1. Open git bash
2. Check the working directory (`pwd` = present working directory)
</p>

  <pre>
     <code class="bash" data-line-numbers="1">
     pwd
     C:\Users\UserName\Desktop\git\project-folder
     </code>
  </pre>

</div>

3. Change the directory to wherever you want the project to live with one of these methods:
   * typing `cd` followed by the location where you want the clone to live
   * or click-and-drag the folder into the bash window

</section>

</section>

---


# Ok, let's give it a try!

Let's clone a repo into directory
   - Go to the repo you want to clone (e.g., [https://github.com/etjernst/Tutorials](https://github.com/etjernst/Tutorials))
   - Click the green Code button, which should drop down & show something like this:
   <img src="/img/README-61cb1c2d.png" width="40%" >
   - Click the clipboard symbol (copies the URL)
   - Back in bash, type
   ```bash
   git clone [thing-you-just-copied]
   ```

> _Hint:_ on Windows, typing `Shift+Insert` is a shortcut for paste in git bash


---

# Tada!

> Navigate to your git folder. What do you see?

* Now tell bash to use the cloned repo as the working directory:

  <div id="left"  data-markdown>
    ```bash
    cd [repo-name-that-you-just-cloned]
    ```
  </div>

<br>
<br>

In the case of my Tutorials repo, this would simply be `cd Tutorials`

> Now you can make changes, stage and commit them!

---

<section>

# Practice staging and committing
> First, don't worry about making mistakes! Remember, git keeps track of **every** version of every file, so I can always roll back any mistakes.


1. Add a new file to the repo inside a folder called _practice_
   - To do this, first create the folder _practice_ using the command `mkdir`
   - Then use the command `touch` to create a new file called `yourName.md`
    ```bash
    mkdir practice
    touch practice/[yourName.md]
    ```
    - The `.md` extension means that it's in markdown format, which is easy to edit in any text editor <br>
    - [Here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is a markdown cheat sheet
      for future reference.
2. Now type `git status` in bash
   > :question: What do you see?

---

#

3. Open up the file with your favorite text editor and add
the text _"About to do my first git commit!"_, then save the file
4. <s> Stage</s> the changes

Back in git bash, add the file to the staging area (first type `git status` again to see what has changed)
   ```bash
   git status
   git add 'practice/[yourName.md]'
   ```
5. Create a `README-practice.md` file in the `practice` folder, add the text _Hello world!_ to the file, and save it
   <details><summary>Code hint below if you need it</summary>

   ```bash
   touch 'practice/README-practice.md'
   ```
   </details>
6. Stage your changes.
   <details><summary>Code hint below if you need it</summary>

   ```bash
   git status
   git add 'practice/README-practice.md'
   ```
   </details>

---

#

7. Now commit your changes

You have staged the changes to both of these files, so they will both be added to the same commit
   > Don't forget to add a commit message summarizing your commit!

```bash
git commit -m "Your very helpful commit message"
```

8. To make sure that you haven't missed any changes from someone else (or past-you from a different machine), `pull` from the remote repo

```bash
git pull origin
```

9. Most likely, you will see the message `Current branch master is up to date.` This tells you it's safe to push your changes to the remote

```bash
git push origin master
```
  > We'll use branches later, but for now just push to the master branch

---

#

10. Ok, now to see the fruits of your labor, go to the repo in GitHub and click on the link that says `# commits`:
![](/img/README-c1ca1f21.png)
    - Click on the `hash` that corresponds to your commit (some combination of letters and numbers)
    - You should see a nice summary of your changes
    - On the right, you can select if you want to see the changes as `unified` or `split` (side by side)

> How cool is that?

</section>

---

<section>

## <a name="basic-workflow">Basic workflow</a>
The steps below outline the general workflow of git

We'll soon complicate it a bit soon with branches, but this covers the basics

1. <s>Pull</s> from the remote repo
```bash
git pull origin master
```
   > Do this each time before you start working, to make sure you aren't missing any updates

2. Make changes, working as you normally would; save changes in your local clone
3. <s>Stage</s> these local changes (add files to the staging area)
```bash
git add [fileA]
git add [fileB]
```

---

#  

4. <s>Commit</s> these local changes to your Git history, adding a logical commit message
```bash
git commit -m "Updated bootstrap routine"
```
5. <s>Pull</s> from the remote repo just in case anyone else made changes too:
```bash
git pull origin master
```
   > :exclamation: I recommend always doing this even if you are working on your own!
   
6. <s>Push</s> your changes to the remote repo on GitHub:
```bash
git push origin master
```





</section>
