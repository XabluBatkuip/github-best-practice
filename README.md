# GitHub Best Practices

This document is a collection of links to advice and best practice for maintaining GitHub repositories. My intention is to have this as an open resource for students, etc. to refer to and update. 

![XKCD git - don't be like this!](https://imgs.xkcd.com/comics/git.png)

## tl;dr

### Repository organisation

* One conceptual group per repository (the conceptual group size/scope may vary between projects)
* Don't commit things that can be regenerated from the code
* Use pre-commit hooks for code-checking (e.g. [`pylint`](https://www.pylint.org/), [`pep8`](https://pypi.python.org/pypi/pep8))
* Use continuous integration where appropriate (e.g. [`TravisCI`](https://travis-ci.org/))
* Use code quality integration where appropriate (e.g. [`Landscape.io`](https://landscape.io/))
* Use test coverage integration where appropriate (e.g. [`codecov.io`](https://codecov.io/gh))
* Don't change the published history
* Avoid large binary files, but if you can't avoid it, use `git-lfs` to store them

### Day-to-day working

* `git pull` before you work; `git push` when you're done
* Review code *before* you check it in
* Make small commits that implement a single logical change and can be described in a simple statement
* Commit early and often
* Write your commit messages as imperative statements - see [this](https://chris.beams.io/posts/git-commit/)
* Use SSH keys to log in if possible

### Workflow
* **Use the workflow that is customary in your group**
* Keep the `master` clean: use branches/forks for development, and pull requests to update `master` 
* Delete branches/forks when done
* Tag releases and submit to Zenodo to get a DOI

![XKCD git commits](https://imgs.xkcd.com/comics/git_commit.png)

## Use the Source!

* Chris Said So: [https://chriskottom.com/blog/2014/02/a-few-modest-best-practices-for-git/](https://chriskottom.com/blog/2014/02/a-few-modest-best-practices-for-git/)
* Frank Carey's Git Best Practice: [https://github.com/frankcarey/git-best-practices](https://github.com/frankcarey/git-best-practices)
* GitHub best practices: [https://blog.bloc.io/github-best-practices/](https://blog.bloc.io/github-best-practices/)
* How to write a `git` commit message: [https://chris.beams.io/posts/git-commit/](https://chris.beams.io/posts/git-commit/)
* Islandora's Git Guidelines: [https://github.com/Islandora/islandora/wiki/Git-Guidelines-and-Best-Practices](https://github.com/Islandora/islandora/wiki/Git-Guidelines-and-Best-Practices)
* Seth Robertson's best practices: [https://sethrobertson.github.io/GitBestPractices/](https://sethrobertson.github.io/GitBestPractices/)
* USGS best practices for code development: [https://github.com/usgs/best-practices](https://github.com/usgs/best-practices)
* Writing good commit messages: [https://github.com/erlang/otp/wiki/Writing-good-commit-messages](https://github.com/erlang/otp/wiki/Writing-good-commit-messages)


## Useful `.gitconfig` aliases

```
alias.lol=log --graph --decorate --pretty=oneline --abbrev-commit
alias.lola=log --graph --decorate --pretty=oneline --abbrev-commit --all
alias.hist = log --graph --pretty=format:'%h %ad | %s%d [%an]' --date=short
```
