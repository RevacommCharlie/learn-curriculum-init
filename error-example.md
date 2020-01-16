## Custom Code Snippets

Custom Code Snippet Challenges allow a student to write code directly in Learn and see the standard output from the test runner. These Challenges provide a student experience that is similar to JavaScript and Python Code Snippet Challenges, but the Curriculum Developer controls the Dockerfile and has all of the flexibility of testable project challenges.

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
* docker_directory_path: /examples/custom-snippets/auth-assessment-custom-snippet-setup

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

<br><br>

## SQL Code Snippet

SQL Snippet Challenges allow a student to write SQL `SELECT` queries against a database defined by a curriculum developer. The submission is evaluated against a supplied test query. The student sees a truncated set of rows as if their query was run from the `psql` interpreter, and the challenge is graded against row and column matches, along with data matches. `ORDER BY` clauses will be respected if they are supplied in the test query.

The database used is:

`PostgreSQL 10.6 on x86_64-pc-linux-gnu, compiled by gcc (GCC) 4.8.3 20140911 (Red Hat 4.8.3-9), 64-bit`

### !callout-info
## Known issue with SQL challenge preview
SQL challenges will render in preview, but will not function if you submit an answer. To test them, publish the repo and try them out attached to an example cohort.
### !end-callout

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique; use a uuid generator-->
<!--'language' is required for type: code-snippet. For sql, use 'sql' -->
<!--'title' is required, string, used when displaying results-->
<!--'data_path' is required, string, must specify a sql file from the root of the repo. It contains everything necessary to create the database and populate the data-->

* type: code-snippet
* language: sql
* id: 7264b4e8-1a0d-44c5-b019-601305617ff8
* title: Absence of a join with Left Outer Join
* data_path: /foodtruck.sql

<!--'question' is required, markdown, the question to be answered-->

##### !question

Given a `users` table with a primary key of `id` and a `trucks` table with a foreign key that references the `users.id` column with `trucks.owner_id`, select all user information from users who do not own trucks, ordered by their last name descending, `users.last`.

##### !end-question

<!--'placeholder' is optional, the starting query in the editor. Not removed when the user starts typing-->

##### !placeholder

```sql
-- Write your query to select users who do not own trucks
select users.* from users
left outer join trucks on users.id = trucks.owner_id
where trucks.owner_id IS NULL
order by users.last desc
```

##### !end-placeholder

<!--'tests' is required for sql code-snippets and contains the query that should answer the question. Student exact-matches are correct, along with data matches. -->

##### !tests

SELECT users.*
FROM   users
       LEFT OUTER JOIN trucks
                    ON trucks.owner_id = users.id
WHERE  owner_id IS NULL
ORDER BY users.last DESC

##### !end-tests

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Testable Project

Just like Project Challenges, but Learn will automatically run tests included in the repo and make the results available to the instructor.

To do this, you need two things --

1. An exercise repo that is setup to run in Docker (covered [here](https://learn-2.galvanize.com/cohorts/667/blocks/13/content_files/Testing-Project-Challenges.md)).
2. A project challenge where the students can submit their fork of the exercise repo (this doc).

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'title' is required, string, used when displaying results-->
<!--'upstream' is required, the upstream repo that will be forked. Set to the branch with the correct Dockerfile and test.sh for running tests-->
<!--'validate_fork' is options, set to true to require that the student submission is a fork of the upstream. If not defined, default is false.-->

* type: testable-project
* id: 358b7964-f097-4c11-a29c-7a3d72ea1098
* title: JS Native Array Methods
* upstream: https://github.com/gSchool/js-native-array-methods/
* validate_fork: false

<!--'question' is required, markdown, the question to be answered-->

##### !question

### JS Native Array Methods

Submit the github repo containing your work on the js-native-array-methods below.

incorrect answer: https://github.com/sperella/js-native-array-methods

correct answer: https://github.com/sperella/js-native-array-methods/tree/correct-answer

##### !end-question

<!--'placeholder' is optional, the placeholder text in the input field. -->

##### !placeholder

https://github.com/<username>/js-native-array-methods

##### !end-placeholder


### !end-challenge

<!----------------------END CHALLENGE----------------------------->
