---
Date: 2022-08-11
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/Bash", "#Topic/Dev/Linux"]
Alias: []
---

# Bash - Install and Setup Git

*Source: *

```bash
# update and upgrade packages
sudo apt-get -y update && sudo apt-get -y upgrade

# install git
sudo apt-get -y install git

# check git version
git --version

# check path for git
which git

# configure git
git config --global user.name "Jimmy Briggs"
git config --global user.email "jimmy.briggs@jimbrig.com"
git config --global init.defaultbranch "main"
git config --global core.longpaths true
git config --global core.excludesFile ""
git config --global core.attributesFile ""

# configure GPG signing keys
git config --global gpg.program ""
git config --global user.signingkey ""
git config --global tag.forcesignannotated true


```

***

## Appendix: Links and References

- [[2-AREAS/Code/_README|Code]]
- [[Development]]
- [[Linux]]
- [[2-AREAS/Code/Bash/_README|Bash]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022

