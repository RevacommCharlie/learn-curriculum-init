# Getting Started

This guide will walk you through a very simple example of publishing a markdown file to Learn. The pages that follow cover:

* Preview and publish markdown files
* Content organization and file types
* Adding challenges
* Creating assessments
* Cohort setup

Each section builds on the previous one, but you may not need them all. You will be able to start publishing curriculum after the first page!

## Previewing Curriculum

This repo has a very basic example unit with a few lessons in the folder `01-example-unit` to get you started. Preview all of the content in this repo by running the following command from the root of the repo. After checking out the contents in Learn, head back here to continue.

```
learn preview .
```

If you are working on a single file, it can be faster to preview just that file rather than the entire repo. To do this, call `learn preview` with the path to the file.

```
learn preview 01-example-unit/01-hello-world.md
```

**Tip**
Add the `-o` flag to the preview command to automatically open the returned URL in a new tab of your browser.

```
learn preview 01-example-unit/02-markdown-examples.md -o
```

## Creating a new page

Now that you have seen some examples, you can create your own page. Create and save a new markdown file within `01-example-unit` and run `learn preview .`. When the preview loads you will see your file added to the example unit. You might have to find it by clicking into the unit and navigating in the left nav.

Feel free to revise your page and re-run the `learn preview` command until you are ready to move on.

## Publishing

So far, you have been previewing work-in-progress so that you can quickly iterate, but your work is not available for real cohorts to use in Learn yet. To publish what you have for everyone, you need to push your work to Github and run a `learn publish` command.

*Push to Github*

1. If this directory is not a repo on Github, set it up as one following the instructions on https://help.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line
2. Make sure that all of you work has been added/committed/pushed to the master branch on github -- `git add -A`, `git commit -m"testing learn publish`, `git push origin master`.

*Publish to Learn*

This command will publish from the remote Githb repo where you just pushed your work.

```
Learn Publish
```

That's it! This repo is now available for anyone to add to a cohort (that process is covered later).

If you want to make change to this or any other curriculum, follow the same process -- make changes, `learn preview [path]`, `git add/commit/push`, `learn publish`.

## Continue

Next: [02-organizing-content.md](02-organizing-content.md)
