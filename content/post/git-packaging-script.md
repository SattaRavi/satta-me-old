---
date: 2016-12-04T23:18:23-07:00
paging: true
title: git packaging script
tags: ['git']
---

Helps create packages for deployment, can be used to create a deployment package for files changed between two [git tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) or two git Head revisions like HEAD³ and HEAD or between commit ids.

the resulting zip can be exploded on to production and the delete script is run to clean up stale files.

{{< gist SattaRavi 66fed939e9c5b5fca3e8f0c910d201d0 >}}

### how does the script work ?

1. The script gets the [git diff](https://git-scm.com/docs/git-diff) between 2 Tags or HEADS or Commit IDs to give a list of all files(with paths) there were either added, modified or deleted.
2. It checks the results for files that were added or modified and pushes them to file_list.
3. It also checks the results for files that were marked as deleted and pushes them to delete_list.
4. If the lists are not empty it then proceeds to create a folder with the timestamp as the name.
5. Using the files from file_list and [git archive](https://git-scm.com/docs/git-archive) it creates a . zip under the above folder.
6. Finally dumps the file paths from delete_list to a txt file under the above folder.