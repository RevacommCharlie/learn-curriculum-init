# Known Issues

1. Custom code snippets are not supported in preview.

## Example Custom Code Snippet

Custom Code Snippet Challenges allow a student to write code directly in Learn and see the standard output from the test runner. These Challenges provide a student experience that is similar to JavaScript and Python Code Snippet Challenges, but the Curriculum Developer controls the Dockerfile and has all of the flexibility of testable project challenges.

### !callout-info
## Known issue with custom snippet challenge preview
Custom snippet challenges will render in preview, but will not function if you submit an answer. To test them, publish the repo and try them out attached to an example cohort.
### !end-callout

<!----------------------BEGIN CHALLENGE----------------------------->

# !challenge

<!--'type' is required, "custom-snippet"-->
<!--'id' is required, string, must be unique within a branch-->
<!--'language' is required. For custom snippets, this only sets the language of the editor that students will type code into. The current list of languages is csharp, html, java, javascript, json, markdown, python, and sql. Contact the software team to have another language added.-->
<!--'title' is required, string, used when displaying results-->
<!-- 'docker_directory_path' is required. The folder in this repo that contains the Dockerfile, test.sh, and tests. -->

* type: custom-snippet
* id: 7ff46e87-d6a6-46b2-9d15-006634247d02
* language: javascript
* title: Auth Assessment Custom
* docker_directory_path: /01-example-unit/custom-snippets/auth-assessment-custom-snippet-setup

<!--'question' is required, markdown, the question to be answered-->

##### !question

This is the custom snippet version of auth-assessment.

The following code can be submitted to test this challenge:

```
const passport = require('passport');
const knex = require('../db/connection');

module.exports = () => {

  /*
    Write your code here
  */

  passport.serializeUser((user, done) => {
    done(null, user.id);
  });

  passport.deserializeUser((id, done) => {
    knex('users').where({id}).first()
    .then((user) => { done(null, user); })
    .catch((err) => { done(err, null); });
  });

};
```

##### !end-question

<!--'placeholder' is optional, the starting code in the editor. Not removed when the user starts typing-->

##### !placeholder
```js
const passport = require('passport');
const knex = require('../db/connection');

module.exports = () => {

  /*
    Write your code here
  */

  passport.serializeUser((user, done) => {
    done(null, user.id);
  });

  passport.deserializeUser((id, done) => {
    knex('users').where({id}).first()
    .then((user) => { done(null, user); })
    .catch((err) => { done(err, null); });
  });

};
```
##### !end-placeholder

## !end-challenge

<!----------------------END CHALLENGE----------------------------->
