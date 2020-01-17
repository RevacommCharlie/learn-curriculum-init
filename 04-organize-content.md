# Organize Content for Learn

There are two primary strategies for organizing content for Learn -- manual and automatic configuration.

#### Option 1: Manual Configuration

Write a `config.yaml` file that defines included content and sequence.

If there is a `config.yaml` file in your repo, it will always take priority over auto configuration.

#### Option 2: Automatic Configuration

If there is _not_ a `config.yaml` file in your repo, Learn will write an `autoconfig.yaml` for you!

Follow a folder and file naming convention and let Learn write an `autoconfig.yaml` for you!

The rest of this guide focuses on the automatic option.

## Folder structure

If you use autoconfig, each top-level folder in your repo will become a single unit (excluding specific folders is covered below). The files within those folders will become lessons and assessments.

```
repo-name/
├----01-first-unit/
│    ├----01-intro.md
│    ├----02-lesson1.md
│    ├----03-lesson2.md
│    ├----04-exercise.md
│    ├----05-checkpoint.md
```

Numbers and punctuation will be removed from folder names, so the example above will make a curriculum block with 1 unit named "First Unit" containing 5 files.

**Note**
You can create multiple units in one repo, but they will always have a fixed order. Only repos can be reordered when setting up a course.

## File types

* Lessons can be .md, .ipynb, or .pdf.
* Units and Lessons are ordered alphanumerically.
* Lesson get their name from the H1 at the top of the markdown, so the filename only appears in the UI if the lesson doesn't have a leading H1.

## Special content types

You can create other content types by following naming conventions.

* Use the extension `.instructor.md` to make a file that is only visible to instructors.
* Use the extension `.checkpoint.md` to make an assessment.
* Use the file extension `.hidden.md` to make a file that starts out hidden and can be made visible later.
* Use the file extension `.resource.md` to make a files that is accessible to students but not included in the left navigation.

For example, your unit could look like this--

```
repo-name/
├----01-first-unit/
│    ├----01-lessonplan.instructor.md
│    ├----02-lecturenotes.instructor.md
│    ├----03-lesson.md
│    ├----04-linked-materials.resource.md
│    ├----05-exercise.md
│    ├----06-quiz.hidden.md
│    ├----07-assessment.hidden.checkpoint.md
```

## Ignoring files and folders

To have the autoconfig ignore top-level folders, or files within those folders, name them with a leading `__` (double underscore).

## Manual configuration

To switch to manual configuration --

1. Create a copy of the auto-configuration so that you can edit it. `cp autoconfig.yaml config.yaml`. Your `config.yaml` will have priority over the generated `autoconfig.yaml`.
2. Modify `config.yaml` to add/remove items, reorder, and set hidden/instructor/resource/checkpoint status.

For help writing or modifying the config.yaml, download the snippets from https://github.com/gSchool/galvanize-flavored-markdown and tab-complete `configyaml` to insert a template.

## Continue

Next: [05-challenges.md](05-challenges.md)
