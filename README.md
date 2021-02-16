- [x] Git Basics
- [x] Linux CLI and Networking
- [x] VCS (hello gitty), GitHub and Collaboration
- [ ] Front-End Basics
- [ ] Intro to HTML & CSS
- [ ] Responsive Web Design
- [ ] HTML & CSS Practice
- [ ] JavaScript Basics
- [ ] Document Object Model - practice
- [ ] Advanced Topics
- [ ] Building a Tiny JS World (pre-OOP) - practice
- [ ] Object oriented JS - practice
- [ ] OOP exercise - practice
- [ ] Offline Web Applications
- [ ] Memory pair game — real project!
- [ ] Website Performance Optimization
- [ ] Friends App - real project!

0.Git Basics<br/>
=================

New to me:<br/>
 + There are three main VCS (Version Control System):<br/>
Git, Subversion, Mercurial.<br/>
	
Surprise me:<br/>
 + Two categories of VCS: Centralized and Distributed.<br/>
 + Status of the document in Google Documents is a link with<br/>
different versions of document.<br/>

I intend to use in the future:<br/>
 - EVERYTHING

<details><summary><strong>Screeenshots</strong></summary>

![Git Basics](img/0_Git_Basics/Version_Control_with_Git.png)

![Git Basics](img/0_Git_Basics/Learn_Git_Branching_2.png)

![Git Basics](img/0_Git_Basics/Version_Control_with_Git.png)
</details>


1.Linux CLI, HTTP<br/>
=================

New to me:<br/>
 + GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate<br/> 
and return the resource.<br/>

 + POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.<br/>

 + PUT: update an existing resource. The payload may contain the updated data for the resource.<br/>
 + DELETE: delete an existing resource.<br/>

 + Post = Put + Delete (sometimes)<br/>

 + HEAD: this is similar to GET, but without the message body. It's used to retrieve the server headers <br/>
for a particular resource, generally to check if the resource has changed, via timestamps.<br/>

 + TRACE: used to retrieve the hops that a request takes to round trip from the server. Each intermediate <br/>
proxy or gateway would inject its IP or DNS name into the Via header field. This can be used for diagnostic <br/>
purposes.<br/>

 + OPTIONS: used to retrieve the server capabilities. On the client-side, it can be used to modify the request <br/>
based on what the server can support.<br/>

 + In HTTP/1.0, all connections were closed after a single transaction. So, if a client wanted to request <br/>
three separate images from the same server, it made three separate connections to the remote host.<br/>

 + To reduce connection-establishment delays, HTTP/1.1 introduced persistent connections, long-lived connections<br/> 
that stay open until the client closes them.<br/>
	
Surprise me:<br/>
 + Post = Put + Delete (sometimes)<br/>

I intend to use in the future:<br/>
 - EVERYTHING<br/>

<details><summary><strong>Screeenshots</strong></summary>
<br/>

![task_linux_cli](img/1_Linux_task_linux_cli/Quiz_Number_1.png)

![task_linux_cli](img/1_Linux_task_linux_cli/Quiz_Number_2.png)

![task_linux_cli](img/1_Linux_task_linux_cli/Quiz_Number_3.png)

![task_linux_cli](img/1_Linux_task_linux_cli/Quiz_Number_4.png)

</details>

2.GitHub and Collaboration<br/>
=================

New to me:<br/>

 - $ git shortlog  --  A quick way that we can see how many commits each contributor has added to the repository<br/>
<br/>
 - $ git shortlog -s -n  -- to see just the number of commits that each developer has made, we can add a couple <br/>
of flags: -s to show just the number of commits (rather than each commit's message) and -n to sort them numerically<br/>
<br/>
 - $ git log --author=Surma  -- display all of the commits by an author<br/>
 - $ git log --author="Paul Lewis"<br/>
<br/>
 - $ git log --grep=bug  -- filter down to just the commits that reference the word "bug"<br/>
 - $ git log --grep="border radius issue in Safari"<br/>
<br/>
To make a PR:<br/>
	+ you must fork the source repository<br/>
	+ clone your fork down to your machine<br/>
	+ make some commits (ideally on a topic branch!)<br/>
	+ push the commits back to your fork<br/>
	+ create a new pull request and choose the branch that has your new commits<br/>
<br/>

 - What might be confusing is that origin does not refer to the source repository (also known as the "original" <br/>
repository) that we forked from. Instead, it's pointing to our forked repository. So even though it has the <br/>
word origin is not actually the original repository.<br/>
<br/>
 - $ git remote add upstream https://github.com/udacity/course-collaboration-travel-plans.git<br/>
<br/>
 - $ git remote -v<br/>
<br/>
 - $ git fetch upstream master<br/>
<br/>
 - $ git rebase -i HEAD~3  -- Если нужно "объеденить n коммита в один", то количество "объединенных" коммитов <br/>
равняется числу(n) после ~(n). Чтобы сохранить эти 3 коммита - можно создать ветку "backup" <br/>
($ git branch backup),а потом объединять.<br/>
<br/>
 - $ git checkout -b foo o/main -- We will checkout a new branch named foo and set it to track main on the remote.<br/>
or<br/>
 - $git branch -u o/main foo<br/>
<br/>
 - $ git push origin main  -- запушили main в origin <br/>
<br/>
 - $ git push origin <source>:<destination> == git push origin foo^:main --можно пушить одну ветку в другую,даже с другим именем<br/>
(if the destination you want to push doesn't exist - give a branch name and git will create the branch on the remote).<br/>
<br/>
 - $ git fetch origin foo~1: bar -- тоже самое, что и push <br/>
(if the destination doesn't exist - Git made the destination locally before fetching) - как и в push <br/>
<br/>
 - $ git push origin :foo  -- delete foo<br/>
<br/>
 - & git fetch origin :bar  -- make a new branch<br/>
<br/>
Surprise me:<br/>
- $ git push origin :foo  -- delete foo<br/>
<br/>
 - & git fetch origin :bar  -- make a new branch<br/>

I intend to use in the future:<br/>
 - EVERYTHING<br/>

<details><summary><strong>Screeenshots</strong></summary>
<br/>

![task_git_collaboration](img/2_GitHub_and_Collaboration/QGitHub & Collaboration.png)

![task_git_collaboration](img/2_GitHub_and_Collaboration/GitHub & Collaboration2.png)

![task_git_collaboration](img/2_GitHub_and_Collaboration/Git upstream.png)


</details>
