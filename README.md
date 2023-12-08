## Description

Open in the browser the GitHub classrooms whose name matches the specified regexp

## Installation

```
gh extension install gh-cli-for-education/gh-classroom-open
```

## Usage

```
✗ ./gh-classroom-open -h 
Opens all the github classrooms matching <regexp> in the browser
Usage: gh-classroom-open [-r|--regexp <regexp>]
       gh-classroom-open [-h|--help]
       gh-classroom-open [-v|--version]
```


## Aliases `gh cd` and `gh pwd`

I have added two aliases to my `gh config` file to make it easier to navigate between classrooms.

```
➜  gh-classroom-open git:(main) ✗ gh  alias list | grep pwd
pwd: '!gh config get current-org'
➜  gh-classroom-open git:(main) ✗ gh  alias list | grep cd 
cd: '!gh config set current-org "$1" 2>/dev/null'
```

For instance:

```
➜  gh cd ULL-ESIT-DMSI-2324
➜  gh pwd
ULL-ESIT-DMSI-2324
➜  gh classroom-open 
```

When no `regexp` is specified, it opens the default classroom as returned by `gh pwd` or it will show the help message
