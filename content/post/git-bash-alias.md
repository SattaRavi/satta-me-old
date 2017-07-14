---
date: 2016-12-18T23:17:41-07:00
paging: true
title: GIT Bash Alias
tags: ['git', 'bash']
---

Long story short, i upgraded my work daily from windows 8 to windows 10, one of the main things i badly wanted to set up was launching sublime from git bash terminal. Earlier i used a method that involved creating a file inside of git installation to host the script that launches sublime.

But i was searching around for a way that was easier for me to setup my terminal if i were to upgrade my OS in the future. Finally came across this gem of an idea to actually use aliases. I then ended up creating a bunch of aliases to make my life easier. Since i put them all on the `.bash_profile` file i can now have them on a GIST or on a repo and have the aliases between computers.

- Create a `.bash_profile` file if it does not already exist under C:\Users\UserName.
- Paste the function below and restart git bash terminal.
{{< gist SattaRavi cb7566a133c84dd49a0a7211050145c1 >}}
- What it does is it creates an alias for a function call that invokes `sublime_text.exe` with an arugument.
- we use the argument to let sublime know which file or folder to open ( like `.` | `../` | `filename.extension` | `folder` )
- And can be used like `subl .` | `subl ../parent-folder-name` | `subl folder-name/file-name.extension`


