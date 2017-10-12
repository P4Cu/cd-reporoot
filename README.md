# cd-reporoot

## Synopsis
zsh plugin to change directory to .repo repository root directory

Forked from cd-gitroot

## How to set up

### Manually install

Put cd-reporoot and _cd-reporoot files somewhere in your $fpath and add the following line to your .zshrc:

```
autoload -Uz cd-reporoot
```

#### For example

```
# download all files
% cd /path/to/dir
% git clone https://github.com/P4Cu/cd-reporoot.git
```

And add the following lines to your .zshrc:

```
fpath=(/path/to/dir/cd-reporoot(N-/) $fpath)

autoload -Uz cd-reporoot
```

### Installing using Antigen
If you use [Antigen](https://github.com/zsh-users/antigen), add the following line to your .zshrc:

```
antigen bundle P4Cu/cd-reporoot
```

### Installing using Zgen
If you use [zgen](https://github.com/tarjoilija/zgen), add the following to your `.zshrc`
```
zgen load mollifier/cd-gitroot
```
to your `.zshrc` with your other `zgen load` commands.

You can set alias to this function.
e.g.

```
alias cdr='cd-reporoot'
```

## Usage

```
cd-reporoot [PATH]
```

If PATH isn't specified, change directory to current .repo repository root directory.
else change directory to PATH instead of it.
PATH is treated relative path in git root directory.

## Options
\-h display help and exit

