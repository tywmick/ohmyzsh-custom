I'm still pretty new at shell scripting, but since discovering [Oh My Zsh](https://ohmyz.sh/), I've gotten pretty excited about it.

Probably my favorite Zsh function I've written so far is [`dev`](/dev.zsh). I organize all the git repos on my local machine under a `~/dev/[owner]/[repo-name]` folder structure, so now, when I execute `dev [owner]/[repo-name]`, it'll first check and see if that repo already exists on my machine. If it does, it'll open it up in [VSCodium](https://vscodium.com/), but if it doesn't, it'll use the [GitHub CLI](https://cli.github.com/) to search for the repo on GitHub, fork it if I'm not the owner, clone it onto my machine, add the correct `upstream` remote if I forked it, and _then_ open it in VSCodium.