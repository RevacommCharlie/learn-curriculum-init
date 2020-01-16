# Assessments

Assessments can be constructed from the same challenges that you add to a lesson. Unlike a lesson, students taking an assessment can't try each answer until they find the right one. They submit the entire assessment at once for grading instead of checking their answers one at a time.

## Syntax

There is an assessment in the example unit that you can look at here -- `01-example-unit/04-checkpoint.md`. This file is built in markdown in the same way that a lesson is, and must include at least one challenge. In order to make it function as an assessment instead of a lesson, name the file something like `[number]-checkpoint.md` or set the type to `checkpoint` if you are manually editing a config.yaml.


## Demo

Use `learn preview` to try out a working example in Learn. Note that markdown files are only rendered as assessments and not lessons if you preview the entire unit.

```
learn preview . -o
```

Then navigate to the Assessment Example.

## Continue

Next: [05-cohort-setup.md](05-cohort-setup.md)
