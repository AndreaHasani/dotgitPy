# Port of kobus-v-schoor/dotgit to Python

## Usage

Consider the following example filelist:
```
.vimrc:desktop,laptop
.vimrc:pi
.bashrc
.foo:server
```
Firstly, there will be two .vimrc files. The first one will be shared between the hosts desktop and laptop. They will both be kept exactly the same - whenever you change it on the one host, you will get the changes on the other (you will obviously first need to do a git pull inside the repository to get the new changes from the online repository). There will also be a separate .vimrc inside the dotgit repository that will only be used with the pi host.

Since no host was specified with .bashrc it will reside inside the common folder. This means that it will be shared among all hosts using this dotgit repository (unless a category is specifically used along with the dotgit commands).

Lastly the .foo will only be used when you explicitly use the category server. This makes it easy to keep separate configurations inside the same repository.

If you'd like to see a dotgit repository in action you can look at my dotfiles where I keep the dotfiles of 3 PC's that I regularly use.

