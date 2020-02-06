# Publish

Publishing takes content from your remote on Github and makes a new curriculum release from it so that anyone can add it to a cohort.

## Publishing = Block Release

If you have developed curriculum for Learn before, you will be familiar with the Block Release process in the Learn app. The Publish command described here does the exact same thing without requiring a trip to the Learn UI.

## Publish the example unit

Feel free to follow along and publish the example unit in this repo. The two major steps are

1. Push to Github
2. Publish to Learn

#### Step 1: Push to Github

1. If your current directory is _not_ a repo on Github, set it up as one under the `gSchool` org, following the instructions on https://help.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line
2. Make sure that all of you work has been added/committed/pushed to the master branch on Github -- `git add -A`, `git commit -m "testing learn publish`, `git push origin master`.

#### Step 2: Publish to Learn

This next command will publish from the remote Github repo.

```
learn publish
```

That's it! A new release has been published for this repo.

* If this is the first time this repo has been published, a new curriculum block was created.
* If this repos had been previously published, a new release was created for the existing curriculum block.

## Recap

Whenever you need to write or modify curriculum--

1. Write/edit files.
2. Run `learn preview [path]` to preview.
3. When you are ready, Git Add/Commit/Push.
4. Run `learn publish` to publish to Learn for anyone to use.

## Continue

Next: `03-organize-content.md`
