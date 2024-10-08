```ini
[user]
    name = Loudog
    email = mxb

[core]
    editor = Sublime Merge
    autocrlf = input

[alias]
	addu = add -u .
	unstage = reset HEAD
	untracked = status -u .
	untracked-at = status -u
	assume-unchanged = update-index --assume-unchanged
	ls = ls-files
    lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %C(dim white)(%an)%Creset %Cgreen(%cr)%Creset' --abbrev-commit --date=relative
	lg2 = log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
	a = apply --index
	unstage = reset HEAD
	p = format-patch --stdout
	co = checkout
	ci = commit
	cp = cherry-pick
	me = merge
	pr = !open "$(git config remote.origin.url)/pull/new/master" # create new PR
	re = rebase
	br = branch
	su = submodule
	rr = reset
  	fm = fetch-merge # fetch and merge
    tree = log --graph --pretty=format:'%C(auto)%h - %s [%an] (%C(blue)%ar)%C(auto)%d'
    bigtree = log --graph --decorate --pretty=format:'%C(auto)%d%n%h %s%+b%n(%G?) %an <%ae> (%C(blue)%ad%C(auto))%n'
    hist = log --date=short --pretty=format:'%C(auto)%ad %h (%G?) %s [%an] %d'
    count = shortlog -sn  # give list of who commited to this repo
    open = !open `git config remote.origin.url` # open repo in browser
    issues = !open "$(git config remote.origin.url)/issues" # open repo's issues in browser
    url =! bash -c 'git config --get remote.origin.url | sed -E "s/.+:\\(.+\\)\\.git$/https:\\\\/\\\\/github\\\\.com\\\\/\\\\1/g"' # show url of remote

[mergetool]
	path = /usr/bin/nvim
	prompt = false
    keepBackup = false

[diff]
	renames = copy
	tool = nvimdiff
[status]
	short = true
	    branch = true
	submoduleSummary = true
	    showUntrackedFiles = all
[color]
	ui = true
[branch]
	autosetuprebase = always
[push]
	default = current
[rerere]
    enabled = true
[pull]
	rebase = true
    autostash = true
[merge]
	; tool = nvimdiff
    ; conflictstyle = diff3
[core]
	editor = nvim
	; excludesfile = /Users/nikiv/.gitignore_global
    # ansi-dark (dark) | GitHub (light)
    # pager = delta --theme='GitHub'
# [interactive]
#     diffFilter = delta --color-only
[github]
    user = loudoguno
; [gpg]
	; program = /usr/local/MacGPG2/bin/gpg2
; [http "https://gopkg.in"]
	; followRedirects = true
[format]
	pretty = %C(auto)%h - %s%d%n%+b%+N(%G?) %an <%ae> (%C(blue)%ad%C(auto))%n
[hub]
	protocol = https
[color "diff-highlight"]
	oldNormal = red bold
	oldHighlight = red bold 52
	newNormal = green bold
	newHighlight = green bold 22
[color "diff"]
	meta = yellow
	frag = magenta bold
	commit = yellow bold
	old = red bold
	new = green bold
	whitespace = red reverse
[rebase]
	autoStash = true
[credential]
	helper = osxkeychain
[blame]
	ignoreRevsFile = .git-blame-ignore-revs
[init]
	defaultBranch = main

```

### Where to Put It
The `.gitconfig` file should be placed in your home directory. You can do this by creating or editing the file at `~/.gitconfig`. Here are the steps to set it up:

1. Open a terminal.
2. Use a text editor to create or edit the `.gitconfig` file in your home directory:

```sh
nano ~/.gitconfig
```

3. Paste the template into the file and save it.
4. Close the editor.

Your Git configuration should now be set up.