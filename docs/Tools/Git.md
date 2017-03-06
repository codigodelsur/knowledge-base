# Git - Version Control System

If you are beginer with git you can check these blogs to get started.

* [What is git](https://www.atlassian.com/git/tutorials/what-is-git) Here you can find a complete guide about git. There you will find beginners article as well as some interesting advance posts.

* [Basic commands](http://rogerdudler.github.io/git-guide/) A list with the most essential git commands.

### Useful tools

Time is precious so here at CodigoDelSur we try to use tools that makes our life more easy. Here there are two tools that can simplify your daily work with git.

* [SourceTree](https://www.sourcetreeapp.com)  is a visual git client, it is very useful to have fast overviews over your repos. On this [link](https://confluence.atlassian.com/get-started-with-sourcetree?_ga=1.261810574.2009675791.1460052474) you will find the tool documentation.  

* [p4merge](https://www.perforce.com/product/components/perforce-visual-merge-and-diff-tools) This is a visual merge and diff tool. [Here](https://gist.github.com/tony4d/3454372) is an installation guide.

# Branch Management
There are many branch management flows that can be implemented. Some flows might work fine with some projects but can be very ineffective with others because of their nature. That’s the reason why there isn't a gold rule to follow when you are creating a branch management flow. Here we are going to describe our git flow that we have been using in many projects and worked really well.


We can distinct between two types of branches: the **main branches** and the **supporting branches**. The main branches are branches that should never be deleted, these branches represents every stage of the code. The supporting branches always have a limited life time, these branches are created to develope a feature, fixing a bug ,etc.

**Important:** Main branches should be protected branches and should require pull request reviews before merging.

###Main branches

`development` Contains all the latest features developed by the team. This is an unstable branch, baisically is constantly recibing features from the developers.

`qa_testing` This branch is where the QA team do theris tests. It contains all the features that will be released to the client or beta testers.

`stage` Holds the latest released version to the client or beta testers. This an stable branch.

`master` Holds the App Store versions. As this is our production branch it must be stable.

###Supporting Branches

`feature` Every time a developer starts a feature, a new branch starting from development must be created. Once the developer finish the feature  and ends testing it, the feature is ready to be merged into development.
These branches should be named as:
feature/[taskid]_taskname

`epic` Baiscially this is a feature branch that contains an epic feature. Epic features baisically are big features that should have an on/off mechanism inside the code(toggle feature). The behaiviour is exact the same as the feature branch and should be named as:
epic/[taskid]_taskname

`bug` Every time the QA team reports a bug, or the developer team detects one, that bug must be treated on a bug branch. These branches must always  be started from the qa_testing branch.
These branches should be named as:
bug/[taskid]_taskname

`hotfix` Every time a bug is discovered on stage or on production we should créate a hotfix branch to fix this issue. The branch starts from stage or master depending on where the bug was detected.
These branches should be named as:
hotfix/[taskid]_taskname
Merges


###Main Branches Merges


`developer -> qa_testing` Once the features that will be added to the build are completed and merged with development, we can merge with qa_testing so then the QA team can test the build.

`qa_testing -> stage` Once the QA team review the build and all the bugs fund were resolved, we can merge from qa_testing to stage.

`stage -> master` Once the Beta testers and the client give us the OK to go to production, we are ready to upload the app to the appstore and this will require to  merge stage with master.

`master -> stage` Every hotfix fixed on master must be merged in stage.

`stage  -> qa_testing` Every hotfix fixed on stage or any aditional code on stage must be merged in qa_testing.

`qa_testing -> developer` Every bug fixed on qa_testing or any aditional code on qa_testing must be merged on developer.


###Supporting Branches Merges

`Feature -> developer` Once a developer finish implementing a task and finish testing that feature, he must merge that feature on development.

`Epic -> developer` Once a developer finish implementing an epic feature and finish testing it, he must merge that feature on development.

`Bug -> qa_testing` Once a developer finish fixing a bug detected on qa_testing he must merge that fix on qa_testing.

`Hotfix -> Stable branch (stage or master)` Once a developer finish fixing a bug detected on a stable branch he must merge that fix on that stable branch.

## References

[http://nvie.com/posts/a-successful-git-branching-model/](http://nvie.com/posts/a-successful-git-branching-model/).

[http://martinfowler.com/bliki/FeatureToggle.html](http://martinfowler.com/bliki/FeatureToggle.html).

[https://www.atlassian.com/agile/branching](https://www.atlassian.com/agile/branching).


