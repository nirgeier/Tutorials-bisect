Bisect Repo
================

The purpose of this repo is the following:

  - Open Git Bash
  - Clone a git repository
  - Feel the Git CLI
  - See the cool bisect command in action
    
    
Usage
--------
 - [Download] git-scm
 - Install git (use the default options and simply click next on every step)
    - (Windows) Right click on your working folder and choose: 'Git Bash Here'
    - (Mac/Unix) Open terminal
 - Copy the clone link
 - Clone the repository :
    - git clone https://github.com/nirgeier/bisect.git

CLI Commands & output
---------------------

```sh
git clone https://github.com/nirgeier/bisect.git 
cd bisect
$ git log --oneline
6348ea3 (20) Fire
07203f2 (19) Fire
75a64b4 (18) Fire
46b7512 (17) Fire
b7e4d71 (16) Fire
1f13307 (15) Fire
ab74477 (14) Fire
bd584e2 (13) Fire
d3e5937 (12) Fire
e083d25 (11) Fire
989b7e7 (10) Water
3d98066 (09) Water
21aae2f (08) Water
61f6ddf (07) Water
d00f208 (06) Water
7745054 (05) Water
7a76bc1 (04) Water
df4c3dc (03) Water
301242d (02) Water
a6141c7 (01) Water

$ git bisect good a6141c7
You need to start by "git bisect start"
Do you want me to do it for you [Y/n]? Y

$ git bisect bad
Bisecting: 9 revisions left to test after this (roughly 3 steps)
[989b7e74aba0e99c1c1e8af9a6d24e6d6729a42a] (10) Water

$ git bisect good
Bisecting: 4 revisions left to test after this (roughly 2 steps)
[1f13307aa9cd00952eda82f316e3ae43749cbff2] (15) Fire

$ git bisect bad
Bisecting: 2 revisions left to test after this (roughly 1 step)
[d3e5937b172e2e978e89379a26d69907cc47394c] (12) Fire

$ git bisect bad
Bisecting: 0 revisions left to test after this (roughly 0 steps)
[e083d25fb917977757e5ba3304e3779e8e237941] (11) Fire

$ git bisect bad
e083d25fb917977757e5ba3304e3779e8e237941 is the first bad commit
commit e083d25fb917977757e5ba3304e3779e8e237941
Author: Nir Geier <nirgeier@gmail.com>
Date:   Mon Jun 23 15:18:54 2014 +0300
    (11) Fire
```

[Download]:http://git-scm.com/downloads
