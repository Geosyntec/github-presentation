

# `git` != **GitHub**

## `git` review

Git is a program on your computer that builds a `.git` directory to track the changes you make and provides tools for tracking changes you make to your code, and for incorporating changes others make to their `.git` directory into yours.
Git commands include:
- commit
- push
- pull
- merge
- rebase
- fetch
- stash
- clone
- ...
```
>git init
>git commit -m "initial commit"




```
--------------------------

## **GitHub** = `git` + web_services
GitHub and similar websites (GitLab, BitBucket) are web services that understand the `.git` directory format and add a few things to help folks collaborate on projects. 
In general, many of the same `git` commands are available but GitHub adds in:
- fork
- pull requests (PR)
- issues
- releases
- CI operations
- free static file server (readme files, docs)
```

>git clone https://github.com/<repo_name_goes_here>


>git push origin develop


>git pull origin main






```
--------------------------
## Real Difference

`git` is a version control system (VCS) to help you manage your code on your machine.

**GitHub** is a "`git`-aware" collaboration web site to help manage git repositories, especially when projects have multiple contributors. 


--------------------------

## When to use `git` or **GitHub**

### when not to use `git`
* if your tool or analysis is not formed of text files, e.g., it's in Excel, `git` likely won't make your life easier.
* if all your code fits in a `jupyter notebook` and if that's good enough for your project, you _probably_ don't need `git`.

### when to use `git`
* _maybe_ when your script has outgrown `jupyter notebook` 
* _maybe_ if your code needs multiple python files to run, that is, one file imports utilities from another file.
* if you're developing a general purpose tool that you want to use for other projects.
  `git` will help save you from yourself as your project grows because "yay it's working" rapidly becomes "oh no, it's broken" and you are going to want VCS to help you figure out why.
* _always_ if you're writing a script or tool that is meant to be shared with, used by, or contributed to by others -- likely via **GitHub**
* _always_ if you're contributing to an existing project, or changing old non-`git` code you found on the server.


### when to use **GitHub**
* if you want to share your code with others
* if you want to contribute to someone elses code
* if you wish to use the tools like GitHub Actions to run tests on every change (Continous Integration)
* if your tool could benefit from the readme and file server capabilities meant to support project documentation


Pretty much all file types are allowed to be committed and stored, so go crazy.

Projects of any complexity can belong in GitHub. 
Use it to post notes for teammates for complicated workflows. 
Use it to remind yourself of how you did that GIS analysis so that you can step through it again next year.
Use it to share a cool analysis notebook you made that is a good example of something you're interested in.


----------------

## Collaboration Patterns On **GitHub**

### Open Issues
  1. **Be Respectful.**
    Just because you found a bug doesn't mean the developers are bad at developing.
  2. Describe the issue and the situation on your machine that lead to you discovering it.
  3. Issues are contributions to projects, not complaints.
    Be prepared to help contribute to the fix if your opening an issue.

### Submit PRs
  1. Alert! an [issue](https://github.com/networkx/networkx/issues/3701) exists in a repo 
  2. fork the repo
  3. make the changes
  4. make new tests and and re-run the test suite
  5. commit your changes to your fork
  6. create a [PR](https://github.com/networkx/networkx/pull/3822) to close the issue

### Releases
  * Help users revert to previously working versions of your code.
  * This is different than the 'commit' history, releases add a tag to the commit that says "this is the spot in the history when we released version 1.2.10" or whatever.

### Documentation
  * show your users how to use your tools


### **GitHub** Actions and webhooks
  * run tests
  * build your software (c, c++, docker images, etc)
  * trigger other pieces of the pipeline, like Continuous Deployment (CD)


------------------------
## Get started with github
1. create an account
2. click 'add repo' and follow the prompts

### Next Steps
* make yourself a personal resume website, hosted for free
  * learn html, css, js to make a static site
  * learn the CI/CD pipelines with a site that uses `flask-flatpages` with python to re-build and re-deploy your site when you change the code.
  * learn js frameworks like `react` or `vue` and `node` build tools like `vite` to build and deploy your free static site.
* Learn about managing "remotes" like `origin` and `upstream`
* Make a contribution to a project, or publish your own project and get help from your team.