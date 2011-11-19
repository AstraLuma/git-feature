git feature
===========

This is my simple helper for feature branches, as defined by [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html). It's primitive and depends on a knowledgable user, but it works. I'm using it in my fork of [tgg-BotSteve](/astronouth7303/tgg-BotSteve).

Commands
--------
`git feature help` prints out a simple usage message. Mostly as a reminder.

`git feature start <name>` creates a new branch and switches to it. If autopublish is enabled, it will also run `publish` (below).

`git feature finish [<name>]` merges the branch (default is the current branch) into master. The branch is not deleted. Merge conflicts can be handled in the usual way.

`git feature publish [<name>]` sends the branch (default: current) to `origin` and sets up syncing in the config file.

Settings
--------
`gitfeature.autopublish` is a boolean value. If true, `git feature start` will automatically publish branches created.
