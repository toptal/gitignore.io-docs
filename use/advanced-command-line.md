---
description: Here are some advanced command line improvements for gitignore.io
---

# Advanced Command Line

### [**@git2samus**](https://github.com/git2samus)\*\*\*\*

this allows invocations as the previous but also permits passing arguments to curl like: gi --proxy somewhere:8080 -- linux python

```bash
function gi() (
    gi_args=()
    for arg; do
        if [[ $arg = -- ]]; then
            curl_args=("${gi_args[@]}")
            gi_args=()
        else
            gi_args+=("$arg")
        fi
    done
    IFS=,
    curl "${curl_args[@]}" http://gitignore.io/api/"${gi_args[*]}"
)
```

### \*\*\*\*[**@git2samus**](https://github.com/git2samus)\*\*\*\*

Adds a check to see if curl or wget is installed.

```bash
if hash curl; then
    curl "${curl_args[@]}" http://gitignore.io/api/"${gi_args[*]}"
elif hash wget; then
    wget -O- "${curl_args[@]}" http://gitignore.io/api/"${gi_args[*]}"
else
    echo "please install curl or wget to run this command" >&2
    exit 1
fi
```

### \*\*\*\*[**@GeorgeErickson**](https://github.com/GeorgeErickson)\*\*\*\*

Bash one-liner

```bash
function gi { curl http://www.gitignore.io/api/"$(IFS=, ; echo "$*")"; }
```

### [**@SantoshSrinivas79**](https://github.com/SantoshSrinivas79)\*\*\*\*

Create a file for the function using vim ~/.config/fish/functions/gi.fish and enter the below code

```text
function gi
  curl -L -s https://www.gitignore.io/api/$argv;
end
```

### \*\*\*\*[**oh-my-zsh**](https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/gitignore/gitignore.plugin.zsh)\*\*\*\*

Provides completion for zsh

```bash
function gi() { curl -sL https://www.gitignore.io/api/$@ ;}

_gitignoreio_get_command_list() {
  curl -sL https://www.gitignore.io/api/list | tr "," "\n"
}

_gitignoreio () {
  compset -P '*,'
  compadd -S '' `_gitignoreio_get_command_list`
}

compdef _gitignoreio gi
```

### \*\*\*\*[**@Phoenix09**](https://github.com/Phoenix09)\*\*\*\*

Improved git alias `tee` to `.gitignore` and accept multiple parameters

```bash
git config --global alias.ignore \
'!gi() { IFS=","; curl -L -s "https://www.gitignore.io/api/$*" | tee .gitignore;}; \
gi'

```

