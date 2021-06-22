Authorship Tests #4

# Authorship Tests #4

Run a series of tests on authorship lists. Create a repository and scan it with several API calls to determine the full extent of identification we can get on authors.

 Create a test repository with each of the following kinds of activity:
* a commit from the main author (set name and email to something unique inside command-line git-config)
* an accepted PR from @rmmilewi
* a rejected PR from a third party
* an issue reporting a bug from @elaineraybourn
* an accepted PR from @frobnitzem that contains a squashed commit log with contributions from a third author
- note: author and committer is distinguished
* a merge-commit by the main author with a third-party's changes

# Scans planned

```
 get_contributors
 get_stats_contributors
 get_collaborators
```
We'll write a short document explaining the test setup
and results from each API call.

# Squash commits

A squash-commit is a particular kind of commit that re-writes the
git history.  For example, say a repository goes through edit steps:
A -> B -> C -> D
and later the author of D wanted to combine several commits
into one commit.  Then, they could re-write their git history to
A -> B -> D'

The new commit, D', is a squash-commit, since it contains all
the changes from both C and D.

If the user pushes the (A -> B -> D') repository, knowledge that
C was a separate commit will have been lost.
Here, I'm creating commit C as Boyana Norris.

Then I'll create commit D as "Mystery Committer <mystery@predictivestatmech.org>". Finally, I'll send the branch as a PR to the main repository.

Ketlin will merge both using the "Squash and merge your pull request commits" feature of Github (https://docs.github.com/en/github/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges).

That documentation states:

When you select the Squash and merge option on a pull request on GitHub, the pull request's commits are squashed into a single commit. Instead of seeing all of a contributor's individual commits from a topic branch, the commits are combined into one commit and merged into the default branch. Pull requests with squashed commits are merged using the fast-forward option.
that the authorship record is gone.
