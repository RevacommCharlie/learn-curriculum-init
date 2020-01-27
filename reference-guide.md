# Reference guide

This is a quick list of the possible commands with the Learn CLI. For more detailed instructions and examples, refer to the Learn CLI Walkthrough by opening `./walkthrough` and following instructions from there.  

## The new publishing workflow

The Learn CLI supports a new curriculum creation flow that works like this:

1. Write/edit files.
2. Run `learn preview [path]` to preview.
3. When you are ready, Git Add/Commit/Push.
4. Run `learn publish` to publish to Learn for anyone to use.

## Possible commands

* `learn help` See a list of commands

* `learn preview`  Allows you to render files in Learn before you committing to Git
  * `learn preview .`  Preview current repo/directory
  * `learn preview <filename.md>`   Preview specific file
  * `learn preview <directory>`  Preview specific directory
  * `learn preview -o <filename.md>` Flag that automatically opens preview once generated--can be added to any preview command


* `learn publish` Publishes the Master branch of a repo to Learn. Commit your local changes to GitHub before publishing. If this repo has been published to Learn before, it will update and create a new release. If this is the first time the repo has been published, it  will create a new block that can be used by anyone in Learn.

## Configuration

Blocks in Learn require a configuration file that defines the content and sequence of a block.

#### Manual Configuration
* Create a config.yaml file that defines the content and sequence of a block. See example structure in `./autoconfig.yaml`
* If there is a `config.yaml` file in your repo, it will always take priority over auto configuration.

#### Automatic Configuration
* If there is no `config.yaml` file in the repo, Learn will write an `autoconfig.yaml` for you.
* Follow a folder and file naming convention to control how the `autoconfig.yaml` is written.
* If you use autoconfig, each top-level folder in your repo will become a single unit (excluding specific folders is covered below). The files within those folders will become lessons and assessments. Numbers and punctuation will be removed from folder names.

```
repo-name/
├----01-first-unit/
│    ├----01-intro.md
│    ├----02-lesson1.md
│    ├----03-lesson2.md
│    ├----04-exercise.md
│    ├----05-checkpoint.md
```
* Use the extension `.instructor.md` to make a file that is only visible to instructors.
* Use the extension `.checkpoint.md` to make an assessment.
* Use the file extension `.hidden.md` to make a file that starts out hidden and can be made visible later.
* Use the file extension `.resource.md` to make a file that is accessible to students but not included in the left navigation.
* To have the autoconfig ignore top-level folders or files within those folders, name them with a leading `__` (double underscore).

### !callout-info
## Need more info?
For more information and examples about anything on this page, refer to the Learn CLI Walkthrough by going to `./walkthrough` and reading through the lessons.
### !end-callout
