# Organizing curriculum for Learn

If you organize your repo like this...

## Simple example

```
repo-name/
├----units/
│    ├----01-first-unit/
│    │    ├----01-lesson.md
│    │    ├----02-lesson.ipynb
│    │    ├----03-lesson.rst
│    │    ├----04-lesson.pdf
```

... Learn will build a curriculum block with 1 unit named "first unit" and 4 lessons.

* Lessons can be any of .md, .ipynb, .rst, or .pdf
* Units and lessons will be ordered alphabetically
* Numbers and punctuation will be removed from units to generate the unit name
* Lessons get their name from the H1

## Publishing

* Run `learn-build`
* To use in curriculum, go to _____

## More complex options

There are other things you can include in your curriculum. If you structure you repo like this ...

```
repo-name/
├----units/
│    ├----01-simple-unit/
│    │    ├----01-lesson.md
│    │    ├----02-lesson.ipynb
│    │    ├----03-lesson.rst
│    │    ├----04-lesson.pdf
│    ├----02-complex-unit/
│    │    ├----01-instructor-lessonplan.md
│    │    ├----02-lesson.md
│    │    ├----03-lesson.ipynb
│    │    ├----04-lesson.rst
│    │    ├----05-lesson.pdf
│    │    ├----checkpoint.md
│    │    ├----resources/
│    │    │    ├----myslides.key
│    │    │    ├----somefile.js
│    │    │    ├----somefile.py
│    │    │    ├----somefile.csv
│    │    │    ├----somefile.sql
│    │    │    ├----another-dir/
│    │    │    │    ├----moardata.csv
```

... Learn will build a curriculum block with 2 units.

* The first unit is the same simple unit for the first example
* the second unit has some additional types of content -- a lesson plan, a checkpoint, and a downloadable resources folder
* Any file with the string "instructor" in the filename will be instructor read-only.
* "checkpoint.md" will be a checkpoint and will be placed at the end of a unit.
* All of the contents of the "resources" folder will be available for students to clone or download.

## Interactive lessons

You can have students answer questions within Learn or submit assignments that they worked on locally. Add Learn challenges to your markdown: learn-2.galvaize.com/docs
