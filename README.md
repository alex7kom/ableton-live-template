# Ableton Live Template Project

A template repository for your next Ableton Live project. Use it to get a proper version control using git and GitHub. Or better, create your own template repository based on this, add your own starter ALS that set up the way you like, and use it as a convenient starting point.

Based on [ableton-experiment](https://github.com/mark-henry/ableton-experiment) and [ableton-git](https://github.com/clintburgos/ableton-git) projects.

## Prerequisites

- macOS (Windows not tested, please let me know if you managed to run it there, so I can provide instructions in this README)
- [git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git) and [git-lfs](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage) installed
- Optionally, a Git GUI you like (I use [SourceTree](https://www.sourcetreeapp.com/), you might try [Github Desktop](https://desktop.github.com/), or countless other free and paid options)

## First time setup

Create a directory for all of your projects, if you don't have it already. For example, let's create `Projects` in your user folder, so the path will be something `/Users/your_username/Projects`. Now, in your projects directory create the file `.gitconfig` with the following contents:

```
[filter "zcat"]
  clean = zcat -f
  smudge = zcat -f
[diff "zcat"]
  textconv = zcat
```

Next, open `.gitconfig` in your home folder and add the following (edit the path so it point to a correct projects directory):

```
[includeIf "gitdir:/Users/your_username/Projects/"]
  path = "/Users/your_username/Projects/.gitconfig"
```

Done!

## How to use

Press **Use this template** on this page and create a new repo. Select **private** repo if any of your assets are going to be proprietary! Then clone it to your _Projects_ directory using your favorite Git GUI/client. Optionally rename `Project.als` to whatever you want, open in Ableton Live and have fun! Don't forget to commit your changes regularly :)

## Caveats

You git GUI/client may ask you to install git lfs in your repository, accept. If you work from command line, you might need to run `git lfs install` in your repo manually.

Don't forget to `File → Collect All and Save` so your samples will be in the repo too.

Check [Github repo size limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [GitHub LFS Limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage) (which apply for files in Samples).

## License

CC0 1.0
