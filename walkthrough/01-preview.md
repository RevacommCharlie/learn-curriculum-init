# Previewing Curriculum

Preview is a new part of the workflow. It allows you to render files in Learn before you commit anything to Git. You can't add students to these previews--they exist to help you iterate on curriculum.

## Preview the example unit

This repo already has contents for a very basic example unit. There are 2 lessons and an assessment in the folder `01-example-unit`. Preview any individual file in this unit like this--

```
learn preview -o 01-example-unit/01-markdown-examples.md
```

Remove the `-o` flag if you don't want a new tab to automatically open in your browser each time.

```
learn preview 01-example-unit/01-markdown-examples.md
```

Instead of just one file, preview the entire unit. You will need to click into the unit to see its contents.

```
learn preview -o .
```

## Creating a new page

Try creating your own page. Create and save a new .md file within `01-example-unit`. Write some markdown and then run

```
learn preview -o [path-to-your-file.md]`
```

Feel free to revise your page and re-run the `learn preview` command until you are ready to move on.

**Note**
If you are already familiar with Learn, you might be wondering how you can do this without modifying a config.yaml. Automatic configuration is a new feature, covered in [04-organizing-content.md](04-organizing-content.md).

## Continue

Next: [02-publish.md](02-publish.md)
