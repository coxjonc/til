If you add a commit and then think better of it, the default command to unstage it is a little ugly: `git reset HEAD --`. Adding an alias to git makes it less ugly of a command:

	git alias.unstage=reset HEAD --
