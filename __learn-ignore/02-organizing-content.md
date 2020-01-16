# Organizing Content for Learn

## Folder Structure

Organize your units as top-level folders and lessons as files within those folders.

```
repo-name/
├----01-first-unit/
│    ├----01-intro.md
│    ├----02-lesson1.md
│    ├----03-lesson2.md
│    ├----04-exercise.md
│    ├----05-assessment.md
```

This example will make a curriculum block with 1 unit named "first unit" and 5 lessons.

You can create multiple units in the same repo, but it is generally a better idea to use multiple repos, each with a single unit, _unless you are sure that a group of units will always be included together in the same order._

* Lessons can be any of .md, .ipynb, or .pdf
* Units and lessons will be ordered alphanumerically
* Numbers and punctuation will be removed from folder names to generate the unit name
* Lesson get their name from the H1 at the top of the markdown, so the filename only matters if lesson doesn't have a leading H1.

## Special types

You can create special file types by following some naming conventions.

* Use the file extension `.hidden.md` to make a file that starts out hidden and can be made visible later.
* Use the extension `.instructor.md` to make a file that is only visible to instructors.
* Use the extension `.checkpoint.md` to make an assessment.

For example, your unit could look like this--

```
repo-name/
├----01-first-unit/
│    ├----01-lessonplan.instructor.md
│    ├----02-lecturenotes.instructor.md
│    ├----03-lesson.md
│    ├----04-exercise.md
│    ├----05-quiz.hidden.md
│    ├----05-assessment.checkpoint.md
```

## Additional customization

The Unit names, included files, content ordering, and hidden/instructor/checkpoint specification can all be customized beyond the naming convention described above. To do this--
1. Create a copy of the auto-configuration so that you can edit it. `cp autoconfig.yaml config.yaml`. If a `config.yaml` is present it will always have priority over the generated `autoconfig.yaml`.
2. Modify `config.yaml` to add/remove items, reorder, and set hidden/instructor/checkpoint status.

For help writing or modifying the config.yaml, download the snippets from https://github.com/gSchool/galvanize-flavored-markdown.

## Continue

Next: [03-challenges-and-assessment.md](03-challenges-and-assessment.md)
