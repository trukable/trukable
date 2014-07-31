# Contributing
##Pull Requests
Only one pull request at a time. If you see a pull request, review it.

##Reviewing
Enforce the guidelines outlined in General Workflow. Comment and reject the pull request if it includes any of the following:
- Commented out code. Delete it or keep it.
- `console.log` statements that are clearly for testing/debugging
- Blatant style guide violations
- Pulling to the wrong branch
- Broad changes - each pull request should address one issue at a time if possible

## General Workflow
For details on some of these steps, see Detailed Workflow section.
1. Fork the repo
1. Clone your fork
1. Add the original repo as an upstream remote
1. Cut a namespaced feature branch from master. Name the branch in the form `prefix/description`:
  - bug/submit-button
  - feat/parameters
  - test/parameters-spec
  - doc/readme
  - refactor/db-utils
1. On notification of pull requests, pull upstream changes
1. Make commits to your feature branch. Prefix each commit like so:
  - (feat) Added a new feature
  - (fix) Fixed inconsistent tests [Fixes #0]
  - (refactor) ...
  - (cleanup) ...
  - (test) ...
  - (doc) ...
1. When you've finished with your fix or feature, pull upstream changes into your branch
1. Resolve any merge conflicts
1. Push your feature branch to your fork
1. Make the pull request from your fork to the organizational repo. DO NOT MERGE THE PULL REQUEST YOURSELF.
1. Wait for a team member to review your changes
1. Fix any issues raised by your code reviewer, push your fixes as a single new commit, and resubmit your pull request
1. After code review and merge, delete feature branch

## Detailed Workflow

### Fork the repo

Use github’s interface to make a fork of the repo, then add that repo as an upstream remote:

```
git remote add upstream https://github.com/trukable/trukable.git
```

### Cut a namespaced feature branch from master

Your branch should follow this naming convention:
  - bug/...
  - feat/...
  - etc.

These commands will help you do this:

``` bash
# Creates your branch and brings you there
git checkout -b feat/search
```

### Make commits to your feature branch. 

Prefix each commit like so
  - (feat) Added a new feature
  - (fix) Fixed inconsistent tests [Fixes #0]
  - etc.

Make changes and commits on your branch, and make sure that you
only make changes that are relevant to this branch. If you find
yourself making unrelated changes, make a new branch for those
changes.

#### Commit Message Guidelines

- Commit messages should be written in the present tense; e.g. "Fix continuous
  integration script".
- The first line of your commit message should be a brief summary of what the
  commit changes. Aim for about 70 characters max. Remember: This is a summary,
  not a detailed description of everything that changed.
- If you want to explain the commit in more depth, following the first line should
  be a blank line and then a more detailed description of the commit. This can be
  as detailed as you want, so dig into details here and keep the first line short.

### Pull upstream changes into your branch

Once you are done making changes, you can begin the process of getting
your code merged into the main repo. Step 1 is to pull upstream
changes to the master branch into your feature branch by running this command
from your feature branch:

```
git pull upstream master
```

### Make a pull request

Make a pull request from your fork and branch to the upstream master
branch, detailing exactly what changes you made and what feature this
should add. The clearer your pull request is the faster you can get
your changes incorporated into this repo.

At least one other person MUST give your changes a code review, and once
they are satisfied they will merge your changes into upstream. Alternatively,
they may have some requested changes. You should make more commits to your
branch to fix these, then follow this process again from rebasing onwards.

Once you get back here, make a comment requesting further review and
someone will look at your code again. If they like it, it will get merged,
else, just repeat again.

Thanks for contributing!

### Guidelines

1. Uphold the current code standard:
    - Keep your code DRY.
    - Apply the boy scout rule (always leave the code cleaner than you found it).
    - Follow [STYLE-GUIDE.md](STYLE-GUIDE.md)
1. Verify the tests are passing before submitting a pull request.
1. Write tests if your pull request contains
   new, testable behavior.
1. Your pull request is comprised of a single commit.

## Checklist:

This is just to help you organize your process

- [ ] Did I cut my work branch off of master (don't cut new branches from existing feature brances)?
- [ ] Did I follow the correct naming convention for my branch?
- [ ] Is my branch focused on a single main change?
 - [ ] Do all of my changes directly relate to this change?
- [ ] Did I rebase the upstream master branch after I finished all my
  work?
- [ ] Did I write a clear pull request message detailing what changes I made?
- [ ] Did I get a code review?
 - [ ] Did I make any requested changes from that code review?
