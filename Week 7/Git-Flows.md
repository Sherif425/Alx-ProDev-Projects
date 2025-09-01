# Project: Git-Flows | Cairo Intranet

ProDev Backend Average: 83.34%

-   [
    
    Back-End Web Development Average: 96.1%
    
    
    
    ](/curriculums/70/observe)
-   [
    
    ProDev Backend Average: 83.34%
    
    
    
    ](/curriculums/86/observe)
-   [
    
    Professional Foundations Average: 94.18%
    
    
    
    ](/curriculums/89/observe)

Week 7

Week 7

-   [Week 0](/projects/102638)
-   [Week 1](/concepts/113077?project_id=102975)
-   [Week 2](/projects/101641)
-   [Week 3](/projects/102758)
-   [Week 4](/projects/101642)
-   [Week 5](/projects/101622)
-   [Week 6](/projects/209)
-   [Week 7](/projects/102965)
-   [Week 8](/projects/102087)
-   [Week 9](/projects/101632)
-   [Week 10](/projects/102428)
-   [Week 11](/projects/102426)

## Advanced shell scripting

[

Advanced Shell Scripting: Automating Tasks and Managing Processes

](/concepts/108709?project_id=101627)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101627)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101627)[

Advanced shell scripting

](/projects/101627)

## Git-Flows

[

Version Control: Advanced Git Techniques and Workflows.

](/concepts/108710?project_id=101629)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101629)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101629)[

Git-Flows

](/projects/101629)

## Containerization with docker

[

Containerization: Introduction to Docker and Container Orchestration with Kubernetes

](/concepts/107383?project_id=101630)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101630)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101630)[

Containerization with docker

](/projects/101630)

## Web Infrastructure

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=302)[

DNS

](/concepts/12?project_id=302)[

Monitoring

](/concepts/13?project_id=302)[

Web Server

](/concepts/17?project_id=302)[

Network basics

](/concepts/33?project_id=302)[

Load balancer

](/concepts/46?project_id=302)[

Server

](/concepts/67?project_id=302)[

0x09. Web infrastructure design

](/projects/302)

## Work Log (Month 2)

[

What Is a Work Log and Why Bother? (a.k.a. Your Brag List)

](/concepts/111671?project_id=102965)[

How to Keep and Update Your Work Log

](/concepts/111674?project_id=102965)[

Update Your Monthly Work Log (Month 2) — ProDev Back-end

](/projects/102965)

# Git-Flows

-   Novice
-   Weight: 1
-   Project over - took place from Aug 4, 2025 1:00 AM to Aug 11, 2025 1:00 AM
-   Manual QA review was done on Aug 11, 2025 3:19 AM
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** 0.0/2 mandatory
-   **Auto QA review:** 2.0/11 mandatory
-   **Altogether:**  **15.38%**
    -   Mandatory: 15.38%
    -   Optional: no optional tasks

**Overall comment:**

Project was failed automatically.

#### Overview

**Git-Flow** is a branching model for Git, proposed by Vincent Driessen, that helps developers manage features, releases, and hotfixes in a consistent and scalable way. It introduces well-defined roles for branches and helps teams coordinate code changes more effectively. Git-Flow is particularly beneficial for large-scale projects where multiple developers work simultaneously on various aspects of the codebase.

Git-Flow revolves around **five primary branch types**:

-   `main` (or `master`) – production-ready code
-   `develop` – ongoing development
-   `feature/*` – new features in progress
-   `release/*` – preparation for production releases
-   `hotfix/*` – critical bug fixes on the main branch

#### Relevance in the Development Process

Git-Flow improves:

-   **Code organization** by clearly separating development stages
-   **Team collaboration** through structured branching and merging workflows
-   **Code stability** by allowing features to be tested and integrated before reaching production
-   **Release management** by isolating release-specific tasks

Git-Flow is widely adopted in **agile and CI/CD** environments, ensuring seamless integration and deployment pipelines while reducing conflicts and regression bugs.

#### Learning Objectives

By the end of this, learners should be able to:

-   Understand the purpose and structure of Git-Flow.
-   Identify the different branch types and their roles.
-   Apply Git-Flow in real-world collaborative development projects.
-   Manage feature development, hotfixes, and release cycles using Git best practices.

#### Learning Outcomes

Learners will be able to:

-   Explain how Git-Flow helps manage large codebases and team contributions.
-   Create and manage branches following the Git-Flow model.
-   Use Git commands to initiate features, releases, and hotfix branches.
-   Integrate Git-Flow into CI/CD pipelines for automated testing and deployments.

#### Git-Flow Best Practices

Best Practice

Description

**Start with `develop`**

Always branch off from `develop` for new features, not `main`.

**Feature Isolation**

Keep each feature in its own branch to reduce merge conflicts.

**Merge via Pull Requests**

Use pull/merge requests for all merges to ensure code review.

**Keep `main` clean**

Only production-ready code goes into `main`. Never push untested code here.

**Tag Releases**

Use Git tags on the `main` branch to mark official release points.

**Use `hotfix/*` for urgent bugs**

Apply emergency fixes directly to `main` via a `hotfix/` branch and merge them back into `develop`.

**Document your workflow**

Maintain clear documentation of your Git-Flow in your project’s README or internal wiki.

#### Common Git-Flow Commands

```
git flow init                   # Initialize Git-Flow
git flow feature start <name>  # Start a new feature branch
git flow feature finish <name> # Finish feature and merge into develop
git flow release start <x.x.x> # Start a release branch
git flow release finish <x.x.x> # Merge release into main and develop
git flow hotfix start <x.x.x>  # Start a hotfix branch
git flow hotfix finish <x.x.x> # Finish hotfix and merge into main & develop
```

#### 📝 Project Assessment (Hybrid)

Your project will be evaluated primarily through **manual reviews**. To ensure you receive your full score, please:

✅ Complete your project on time  
📄 Submit all required files  
🔗 Generate your review link  
👥 Have your peers review your work

An **auto-check** will also be in place to verify the presence of core files needed for manual review.

##### ⏰ Important Note

If the deadline passes, you won’t be able to generate your review link—so be sure to submit on time!

We’re here to support your learning journey. Happy coding! ✨

##### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Show quiz)

##### Question #0

Which Git command would you use to combine changes from two branches without altering the commit history?

-   git cherry-pick
    
-   git stash
    
-   git rebase
    
-   git merge
    

---

##### Question #1

What is a key difference between merging and rebasing in Git?

-   Rebasing applies changes from one branch on top of another, while merging combines them.
    
-   Rebasing creates a new branch, whereas merging deletes branches.
    
-   Merging rewrites commit history, while rebasing does not
    
-   Merging always results in conflicts, whereas rebasing never does
    

---

##### Question #2

What does the `git cherry-pick` command do?

-   It applies a specific commit from one branch to another.
    
-   It creates a new branch with selected commits
    
-   It merges two branches together.
    
-   It saves uncommitted changes for later use.
    

---

##### Question #3

In the .Gitflow Workflow, what is the purpose of the develop branch?

-   To serve as the main branch for production-ready code
    
-   To back up all commits
    
-   To store experimental features
    
-   To integrate all feature branches before merging into master
    

---

##### Question #4

What is the primary purpose of `git stash`?

-   To permanently delete uncommitted changes
    
-   To merge changes from one branch to another.
    
-   To save your work temporarily without committing it.
    
-   To apply a commit from one branch to another.
    

---

##### Question #5

Which Git workflow is most suitable for small teams and simple projects?

-   Forking Workflow
    
-   Centralized Workflow
    
-   Gitflow Workflow
    
-   Feature Branch Workflow
    

---

##### Question #6

When would you typically use `git cherry-pick`?

-   To reapply stashed changes
    
-   To undo the last commit on a branch.
    
-   To merge feature branches into the main branch.
    
-   To apply a single commit from one branch onto another branch.
    

---

##### Question #7

In the Forking Workflow, where does each developer maintain their own copy of the project?

-   In their personal forked repository
    
-   In a shared feature branch
    
-   On the master branch of the main repository
    
-   On the develop branch of the main repository
    

---

##### Question #8

Which command is used to retrieve stashed changes in Git?

-   git cherry-pick
    
-   git merge stash
    
-   git apply
    
-   git stash pop
    

---

##### Question #9

Which of the following branches is considered the default branch in the Gitflow Workflow?

-   develop
    
-   release
    
-   master
    
-   feature
    

## Tasks

##### 0\. Setting up gitflow

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Understand and initialize a GitFlow workflow

**Instructions:**

-   Install git-flow if not already installed. Steps [here](/rltoken/gMp_VwUHsCWhFKF8tHqqKQ "here")
    
-   Create an empty repository `ALXprodev-advanced_git`
    
-   Clone your repository to have it available locally.
    
-   Create a branch `develop`
    
-   Push the develop branch to the remote repository
    
-   Initialize Git Flow within the repository using default settings i.e `git-flow init [-d]`
    
-   Create an empty `README.md` file
    
-   Commit your file to staging and Push
    

**Repo:**

-   GitHub repository: `ALXprodev-advanced_git`
-   File: `README.md`

Check submission View results

##### 1\. Creating a feature branch

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**: Learn how to work with feature branches in GitFlow.

**Instructions:**

-   Create a new feature branch `feature/implement-login` from the `develop` branch
    
-   In the `feature/implement-login` create a new directory called `login-page`, inside it create a `README.md` file with the message: `Login Feature Coming soon`
    
-   Commit your changes and push to github
    
-   Use commit message `feat: scaffolding login page`
    

**Repo:**

-   GitHub repository: `ALXprodev-advanced_git`
-   File: `login-page/README.md`

Check submission Mark submission : in progress... : an error occurred View results

##### 2\. Creating a Release Branch

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**: Understand the release process in GitFlow.

**Instructions:**

-   Create a new feature branch `feature/implement-signup` from the develop branch and create a directory called `signup-page` with a README.md file with the message `feature coming soon`
    
-   Commit the changes and push to github
    
-   Merge the 2 branches to the `develop` branch. Fix conflicts if any
    
-   Create a new release branch `release/1.0.0`
    
-   Make changes to `signup/README.md` file by adding the following text:`” data requirements: email, firstName, lastName, profilePic]”` inside the release branch
    
-   Commit and push changes to github then merge the `release` branch to the `main` branch and the `develop` branch
    
-   Tag the release with `v1.0.0` and push the tags to the remote repository
    

**Repo:**

-   GitHub repository: `ALXprodev-advanced_git`
-   File: `login-page/README.md, signup-page/README.md`

Check submission Mark submission : in progress... : an error occurred View results

##### 3\. Git Hooks and Automation

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Implement Git hooks to automate parts of the GitFlow process.

**Instructions:**

-   Implement a pre-commit hook in the file .git/hooks/pre-commit that checks if each directory in a Git repository has a README file
    
-   Implement a post-merge hook that logs the merge after completing a merge into the main branch.
    

Hint: Read more [here](/rltoken/frWTLzVrBwL4DU9LP24agQ " here")

**Repo:**

-   GitHub repository: `ALXprodev-advanced_git`

Check submission View results

##### 4\. Manual Review

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Repo:**

-   GitHub repository: `ALXprodev-advanced_git`

View results

Ready for a new review

[

Back

](/concepts/111449?project_id=101629)

[

Next

](/concepts/107383?project_id=101630)

Copyright © 2025 ALX, All rights reserved.