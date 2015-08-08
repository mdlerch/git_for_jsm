% Using git and online hosting for for efficient collaboration in scientific research
% Michael Lerch


Objectives and Goals
--------------------

- I went through a few iterations in putting this talk together.
- And I received some valuable feedback, and I've adapted my slides based on that feedback.
- I quickly want to go over the goals and assumed starting point for my presentation.

- It sounds like people are, at least, aware of the existence of something called `git`
- They know it is used for some sort of "version control"
- They know that it is paired with github or maybe bitbucket
- But maybe aren't quite sure about the difference between git, github, and bitbucket
- People seem vaguely aware that the _should_ use git, but aren't aware how it can improve collaboration and workflow
- Lastly, people are curious what sort of technical expertise it requires to use, or at least, get started with git.

- My goal for this talk is to clarify these points, and hopefully inspire people to start using git.

- I do not intend to teach people how to use `git`
- There are already a number of resources to learn git on the web
- And I believe my target audience would benefit greater from a big picture than hearing me talk about the details and commands.


`git` vs github
---------------

- First let's talk about the difference between git and github

- git is software that runs on your personal computer
- It is used to keep track of projects that are composed of computer files
- Specifically, git keeps track of the history or evolution of a project
- We call a project under git control a repository.
- The repository consists of commits, which are like snapshots of all the files in your project.
- git lets you easily see or even revert to earlier versions of your project
- For a given project, you and your collaborators will all likely have their own git repository of that project.
- git is also used to connect to these other repositories to access the work.

`git` vs github
---------------

- So git is software that you are running your own computer that does version control
- github, and I am using "github" to mean github or bitbucket or gitlab,
- is a website that hosts, with special features, git repositories
- So, while you and your collaborator both have git repositories on your computer, getting your computers to talk directly might take some technical knowledge
- However, using github as an intermediary, centralized location is trivial
- And these websites provide more than just repository hosting
- They have a variety of collaborative and graphical tools

- So in summary, git is something you run on your computer and does NOT require github
- github makes collaborating and dissemination much easier.

Differentiate hosting providers
-------------------------------

- So how do you choose among github, bitbucket, and gitlab?
- So using one doesn't preclude another.
- You can host one project on github another on bitbucket, etc.
- You can even host a single project on each service
- But it's best if you have a single service clearly designated as the true home of the project.

- So why would you choose one of these over the others?
- The collaborative features offered by all the providers are pretty similar.
- The interfaces are slightly different but also pretty similar.
- The biggest difference is how they handle public and private repositories.
- Public repositories means that anyone can go and look at your repository.
- Private means that only invited users can see your repository.
- You may have sensitive data or otherwise work that you want to keep private or at least start as private and then eventually make public.
- Consider whether it really is important that your project is private.

- First github, which is probably the most popular and generally comes up with new features first.
- On github you can have an unlimited number of public repositories
- but, unless you pay, no private repositories (though academics or maybe just students can get free elevated accounts)
- If you are willing to pay the pricing tiers determine the number of private repositories you can have.

- On bitbucket, the basic account also gets you unlimited public repositories
- But also you get unlimited private repositories, but only up to 5 collaborators
- Their pricing tiers are based on the number of collaborators you want per repository

- Lastly, there is gitlab which is relatively new
- They seem to offer both unlimited public and private repositories
- Though they also exist at gitlab.com they essentially offer their website source code for free
- So your IT manager may have a locally hosted version of gitlab.
- Even at my school in Montana, we have our own gitlab service.

An example
----------

- Let's look at an example project.
- So I'm going to show you a project that me and a fellow grad student are or were working on.
- We are using github, but everything you'll see can be done with any of github, bitbucket, and gitlab, just maybe look a little different.
- It should be pretty clear how this can generalize to many people and also how even a single contributer project could benefit from git and github.

My computer
-----------

- So let's just look at what's on my computer
- Here's the folder that contains my project
- I have a bunch of files and a bunch of folders all with their own files.
- Your project may contain fewer files or more--doesn't matter.
- But what you SHOULD NOT have is something like this


Bad idea
--------

- Do not manual version your files
- You are using git now; git takes care of your versioning

My computer
-----------

- So this is what my project looks like.
- So what happens when I add git to the mix?

Add git
-------

- Nothing happens to my files.
- But now I have this dot-git folder.
- That contains all the meta data, history, etc.
- Don't do anything with that dot-git folder.
- That's the place that git does it's work.

Repositories
------------

- So we set up git so we saw, I now have a repository there on my computer
- I'm going to push this repo up to github as well to act as the project home.
- The centralized place where anyone, particularly, John, can access.
- So John's going to do work, too, so he will also have a repo on his computer.
- We also have a repository hosted under John's github account where I can see and integrate the work John has done into the main repository
- John's github repo is not really necessary, _trusted_ users can be granted write access to my repo as well.

Github
------

- Let's take a quick look at what the repo looks like up on github
- So the same content is also on github.
- All my files and folders are there, but github has extracted some information out of that dot-git folder to tell me things like
- There have been 148 commits in this project
- There have been 2 different people who have made contributions

Doing work?
-----------

- So now that I am using git, how do I do work?
- That doesn't change
- I work exactly like normal, open up a file, make changes and save them.

You have to _use_ `git`
-----------------------

- After making "enough" changes, then I USE git
- I have to commit my changes to create a new snapshot, a new entry in the history
- After, my local repository has a new commit in it's history so I need to PUSH that up to github
- That way John can now see and obtain my changes, at his convenience
- He will then pull those new commits from my repository into his repository

Why is this better than dropbox or google drive?
------------------------------------------------

- The healthy skeptic will ask now why is this better than dropbox or google drive
- With those services, everything is automatically uploaded and propagated.
- Well, it's convenient to have this nice labeled history
- to be able to click and see how the files have changed
- what your files looked like a while ago, revert to an older version, etc
- But the biggest immediate advantage is control.
- You are in charge of your files.
- You pull in changes when YOU want.
- You push out changes when YOU want.
- People can work simultaneously without stepping on each others toes
- git also allows much more powerful workflows such as branching


Branching
---------

- I'm just going to talk briefly about this
- In my experience, branching is where beginners become convinced
- Branching means diverging from the main history
- You could do this for a number of reasons.
- You want to do some experimental work that may or may not become "real"
- You want to do something that's going to take a while, and don't want others to be worried about what you are doing in the mean time.
- Or similarly, you and others are both doing work and you don't want the history of the project to be intermingled
- After you finish up your branch, if it's bad you just get rid of your branch with nothing to worry about, or if it's good you merge the commits from that branch into the main history.

Is `git` hard to use?
---------------------

- So there's a lot of power here with git.
- How hard is it to use?
- Well, do you know about files and folders on a computer?
- And do you have a different folder for each project?
- If so, you can use git.
- Without doubts.
- However, as you try to learn about git you will undoubtedly run into pictures like this...

Is `git` hard to use?
---------------------

- There will be rounded boxes with weird strings of letters and numbers
- Square boxes that are presumably a different element than the rounded boxes
- And a whole bunch of arrows that, seem to point backwards
- And you will get confused.

Is `git` hard to use?
---------------------

- The problem is that git is feature-filled and extremely powerful
- And as a beginner it can be difficult to determine what is important
- You won't know how much of git you need to know before you can become operational.
- Having a collaborator who knows what he or she is doing is invaluable for the beginner
- A person with the computer competence I've described with a collaborator who knows what they are doing can be up and running with git almost immediately
- The key is just introducing the functionality as needed.

Collaborating on github
=======================

Reviewer Comments
-----------------

- "Please use track changes and save the document with your initials"
- "**Person A** and **Person B** are off the hook"
- "**Person C** and **Person D** please look at the comments for points I
  want you to work on"
- "Here's what I've done so far; I'm not finished but wanted to share what I
  have done so far"

Using Issues on github
----------------------

- Your TODO list lives at the _same place_ as the project itself

![](./img/issues.png)

Using Issues on github
----------------------

![](./img/anissue.png)

Why aren't you using `git` already?
===================================

Classical Conditioning
----------------------

\begin{itemize}
    \item The reward (or punishment) is too far separated from the act!

    \item Must actively train one's self to use `git`
\end{itemize}
