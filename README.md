Authorship Tests #4


Run a series of tests on authorship lists. Create a repository and scan it with several API calls to determine the full extent of identification we can get on authors.

 Create a test repository with each of the following kinds of activity:
* a commit from the main author (set name and email to something unique inside command-line git-config)
* an accepted PR from @rmmilewi
* a rejected PR from a third party
* an issue reporting a bug from @elaineraybourn
* an accepted PR from @frobnitzem that contains a squashed commit log with contributions from a third author
- note: author and committer is distinguished
* a merge-commit by the main author with a third-party's changes
 get_contributors
 get_stats_contributors
 get_collaborators
 write a short document explaining the test setup and results from each API call.