% Using git and online hosting for for efficient collaboration in scientific research
% Michael Lerch


Objectives and Goals
--------------------

- Many have heard about `git` and want to use it
- Differentiate between _github_, _bitbucket_, etc
- How does collaboration work with `git`
- What if I come and go frequently?
- What technical prowess does one need to use `git`

Non-goals
---------

- Teach you to use `git`

- Plenty of learning resources already


`git` vs github
---------------

`git`

- `git` is software you run on your computer
- Keep track of history of your project
- Connect to and integrate changes in other repositories

`git` vs github
---------------

github (bitbucket, gitlab)

- github is a website
- host a repository at a centralized location
- incorporate collaborative tools
- one can use `git` without github
- github makes collaborating much easier


Differentiate hosting providers
-------------------------------

You can use all of these.  Simultaneously even.

- github

    - Probably most popular
    - unlimited free _public_ repositories
    - _private_ repository pricing based on number of repositories
    - Built-in website hosting

- bitbucket

    - Supported by Atlassian
    - unlimited free _public_ repositories
    - unlimited free _private_ repositories (up to 5 collaborators)
    - _private_ repository pricing based on number of collaborators

- gitlab

    - Your institution may host a gitlab server for unlimited _public_ and
      _private_ repositories

An example
----------

- Project on which I work with one other person
- It should be simple enough to imagine how this workflow _easily_ scales to
  many more people
- It should be easy to see how aspects of this workflow appeal to a single
  contributer as well

Repositories
------------

- I will work on my computer so I need a repository on my computer
- A repository under my github account acts as the project home
- John will work on his computer so he has a repository on his computer
- A repository under John's github account allows me to integrate _John's_ work
  to the main repository under my github account.
- _Trusted_ users can also be given _write_ access to the main repository

My work
-------

- Write some more code, apply edits to a document, etc.
- _commit_ my changes.
- _push_ my changes up to github
- John can now see and obtain my changes

How does John get my changes?
-----------------------------

- _pull_ commits from a remote repository into your local repository

Why is this better than dropbox or google drive?
------------------------------------------------

- Labelled history
- Collaborators update _when they want_
- Collaborators release updates _when they want_
- John and I work simultaneously without stepping on each other's toes

Using issues
------------

- Keep track of your TODO list
- Your TODO list lives at the _same place_ as the project itself
- Dealing with reviewer comments

Reproducible research
---------------------

- 

























