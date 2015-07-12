Script for my JSM talk

This is a talk about git
------------------------

This is a talk about git.
For the most part, everything we'll talk about here is applicable to other version control systems.
git seems to have become the most popular VCS.
Some others that you have heard of are svn (or subversion) and hg (or mercurial).
If you are interested in incorporating a VCS into your workflow, I would recommend going with git unless you have a very specific reason to go with something else.

Preliminaries
-------------

OK. Let's make sure that everyone has the basics down before I dive into this talk.
Scientists use computers to do science.
More than that, almost all of science is done on computers now; not just to control machinery but to process and analyze data.
Just like a lab book should be kept to keep track of experimental steps in a lab, the steps used in cleaning data and performing analyses should be kept.
If you use something like R, keeping track of this is relatively straight-forward.
Write a script or multiple scripts that give R the instructions on how to go from the raw input data to the output: which could be statistical results, a manuscript, a website, or any other final product.

So for a given project, we have a collection of these files.
The files are like the content of a lab book.
git is like the lab book itself.
However, unlike in the lab book, the files might evolve over time: a new analysis or new data, multiple people working on the files, etc.
Congruently, git has to be powerful.
To be good scientists, we have to track how our project evolves over time.
We have to have efficient means of collaborating.
And this is what git provides.
Git is a computer program that keeps efficiently manages the evolution of project--a collection of files.

What to expect
--------------

What should you expect out of this talk.
I'm not interested in teaching you how to use git.
There are plenty of resources on the internet to do that.
I want to convince or inspire you to add git to your workflow.

Why aren't you already using git?
=================================

I bet many of you have heard of git and maybe even a number of you have tried it out a little bit.
But you maybe haven't fully committed.
If I'm going to convince you to use it, we need to understand why you aren't currently using it.

Classical conditioning
----------------------

And that reason is because of classical conditioning: how we learn.
In order to reinforce good behavior we need a reward.
In order to reduce bad behavior we need a punishment.
And the reward or punishment must be associated with the act in question.
git is like exercising or eating your vegetables.
The benefits are not immediate.
In fact, you may find the actual act to be painful, especially when you are just getting started.
You need to train yourself to use git.
If you are the type of person that values organization, then this may come easy, it's kind of like the endorphins provided by exercise.

OK, so let's inspire you to start your git regimen

What do your files look like on your computer
=============================================

First, if you browse to a recent project on your computer, what do the files look like?
Perhaps something like this:

Why do we do this
-----------------

What we are looking at here is just two different files.
OK, it looks like we have our initial script, OK version 1, make sense, version 2, oop, now we are versioning by date not number.
Ah, the final script.  But there's a new dated scripted that is not labelled final...I probably new what I was doing back then, but two months later, I don't recall which is which.

And of course writing a manuscript.  Yes, a whole sequence of my versioning, plus someone else's edits.  How do I get this all merged together?  I should probably just ignore what that person said.

And anyway, how does stuff like this even happen?

How does this even happen?
--------------------------

Our date versioning system doesn't even match when my computer thinks the files were last modified!

Goodness, this is confusing even for me!
I just hope no one wants to see my work.
There's no way I can just hand this off.

Heart is in the right place
---------------------------

Well, if that's what your files look like, your heart is in the right place.
Why do we have all this mess?
Sometimes we _do_ need to revert.
The history of a project is important.
It is a huge part of the scientific process.
But managing this kind of stuff is very difficult, even for the author.
When this is what you have, sharing is difficult to say nothing of collaborating.
And don't forget that person we all collaborate with: our future selves.

So let's get rid of this problem with git.

First steps in git
------------------

We are going to turn our project into a git _repository_.
A repository is the phrase for a project in git parlance.
The content of a repository is a collection of commits.
A commit is a snapshot of contents of the project (so all the files).
It makes sense to create a commit each time a new idea is added, something is changed or fixed, etc.
This way, we have the complete _history_ of the project: a bunch of snapshots or commits of how we got to where we are now.
Here's a picture of our files under git management.
Each file is now a single file.
The files aren't sprawling out via versioning all over the place.
However, our history is still there.
It's getting tracked automatically in that .git folder.
Here's a visualization of the history.
Each of these icons represent a new commit.
I can see who made the commit and read a short description of what the purpose of that commit was.
All of this meta data is stored automatically.

Second steps in git
-------------------

Not only do I have the snapshots and short description of changes, I can see the literal difference between snapshots with a diff.
If you are using the by hand versioning method, you might like to have specific milestones noted.
You can do that in git with tags which essentially tag a specific commit with a name so it is easy to reference that snapshot of your code.
I point this out because I've noticed that when people first start out with git, they seem to want this feature, but, for most of you here, it's probably not something that you'll really end up using.
Just a remnant of an old way of working.

OK, so we've cleaned up our project files and this will eliminate all sorts of headaches.
Now, every file is the current file.
And yet, the past is easily accessible.
This should save YOU many headaches.

Sharing with others
===================

So let's now talk about sharing with others.

Sharing
-------

Again, good file organization is good for you, the main author, and it's just much easier and quicker to share a clean file system with others.
But there are additional benefits of using git in collaborations.
So first, think about how you currently share files?
Do you use email?
How often are you spamming your collaborators?
Every little change?
Only major changes?
Are you resending the whole project or just individual files as they change?
Super annoying.  And let's hope noone misses an attachment...

Do you use dropbox or google drive?
I don't know what the actual terms of these services are, but when using such services, I don't feel like I own the file.
Any bozo I'm collaborating with makes any change?
Boom.
It's propagated down to me.
I want to manage my files, not have my files manage me.

Third steps in git
------------------

With git we use online repositories.
The online repository is the same repository that I have on my computer, but it's hosted online where others have access to it.
The major hosting providers are github, bitbucket, and gitlab.
Your institution may even host their own.
The online repository is excellent because the whole repository is right there.
You don't need to manually email things to people or worry about files getting lost or going missing.
You also don't need to interrupt peoples work by forcing them to update to latest versions whenever you make an update.
Further, all these providers I've mentioned offer an array of additional features besides just hosting the git repo.
It's also worth mentioning that dealing with both your local repository on your computer and a remote repository up on, say, github is baked right into git.
It's one of the fundamental principles of git to be able to reference different repositories.

Getting something back (workflow)
=================================

So, we all are familiar with email attachments.
Like I said, they are annoying to deal with, but we know how to deal with them.
So let's talk about the basic principles of how to use or interface with a remote repository up on github.

Fourth steps in git
-------------------

Here are your two verbs or commands: push and pull.
When you've worked on the project and made a series of commits, you will want to push your commits up to github.
Pushing says, make commit history on the remote repository be the same as the commit history on my repository.
If you've made one additional commit, that commit will be pushed.
If you've made three additional commits, then those three will be pushed.

Now suppose that instead, your collaborator is the one who has made new commits.
Now, the remote repository on github has additional commits and you will need to PULL them down to your local repository.
So, YOU own your files.
You push and pull when you want typically, it's good to push often.
However, if you are away the project, you can always get up to date by pulling changes down when you get around to it.

Fifth steps in git
------------------

And now we get to some of the real power of git: branching and merging.
Depending on how you work, this may or may not be applicable, but it is definitely important that I mention it.
This picture is a graphical representation of a history of commits.
The C0, C1, etc are the commits, the arrows, here, point to the previous commit.
So, let's assume we've done a bunch of work and created a repo and pushed it up to github and now have given a collaborator access.
BUT...
we don't want to bring this collaborators edits in immediately, either because we are simultaneously working on something as well, or the collaborator wants feedback on his or her changes before they become official, or any other reason.
So, the collaborator works on a new BRANCH, and we graphically see the splitting here at C3 and C4 from C2.
Our work is based off of commit C2 and so is the work of our collaborator.
Eventually the collaborator makes some edits, we approve them--maybe after a small series of revisions--and now we are ready to bring them into the main, MASTER branch.
We do this by MERGING that branch into the MASTER branch.
This is automatically handled by git.

As we discussed earlier, with git we think of the files as the current version and the history is there, but just tucked out of the way.
So, whenever we, or someone, wants to do some work but we don't want to force this work onto all the collaborators YET, it makes sense to branch.

This is probably obvious, but I'll say it anyway, using branches is so much easier than say getting emails from 3 different collaborators who have all made changes and trying to reconcile those changes.

So that maybe begs the question that yes, you can have many branches.

git handles complicated work patterns
-------------------------------------

So take a look at this complicated branching pattern.
This is not an example of some crazy branching adventure that happened one time.
This is a branch based workflow that some people recommend to always use!
And git handles it cleanly.
For most of us in the room, this is not a picture that will represent how we will work, but it should be reassuring that there's enough power in git to easily handle our branching strategies that will be simpler.

Summary
=======

OK, so we've covered the basic use of git and talked about the advantages.
Let's just quickly summarize.

Summary
-------

Your git repository is your lab book for the computing end of your project.
Your history is all there and recorded, but not in your way.
Commits are the elements of the history: discrete snapshots of the files in your project.
Comparisons, reverting, and just seeing the evolution of the project are automatic.
github, bitbucket, or any online hosting of your repository is better than email, dropbox, etc.
Branching makes collaboration efficient, and honestly, fun.

But, the most important thing is to

MAKE YOURSELF USE IT
====================

It is SLIGHTLY easier to save as my script underscore today's date than it is to git commit message Changed units on plot.
But when you get annoyed with your manual date versioning, make sure to properly associate that annoyance and train yourself to use git.






































