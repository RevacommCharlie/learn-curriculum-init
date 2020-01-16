
## Multiple Choice

Multiple Choice challenges allow a student to submit a single answer to a multiple-choice question.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'title' is required, string, used when displaying results-->

* type: multiple-choice
* id: 4fb73ef6-1492-45c9-b937-fe718cb80fea
* title: Example Multiple Choice Challenge

<!--'question' is required, markdown, the question to be answered-->

### !question

Which of these cities is home to a Galvanize campus?

### !end-question

<!--'options' is required, a bulleted markdown list, the options the student selects the correct answer from-->

### !options

* Chicago
* Denver
* Fort Collins
* Miami

### !end-options

<!--'answer' is required, the correct answer, must exist in the options-->

### !answer

Denver

### !end-answer

<!--'explanation' is optional. Shown after the student correctly answers the question.-->

### !end-challenge

<!----------------------END CHALLENGE----------------------------->


<br><br>

## Checkbox

Checkbox challenges allow a student to submit multiple answers to a multiple-choice question.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

* type: checkbox
* id: a2b0dd37-4d72-490f-ba26-c6e7b08d21a0
* title: Example Checkbox Challenge

##### !question

Mark all of the cities that are home to a Galvanize campus.

##### !end-question

##### !options

* Portland
* Denver
* Los Angeles
* Miami

##### !end-options

##### !answer

* Denver
* Los Angeles

##### !end-answer

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Short Answer

Short-answer challenges allow a student to submit a short answer, usually a single word, as the answer to a question. By default, the answer is evaluated as a case-insensitive exact match, but can also be evaluated as a regex.

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a single markdown file-->
<!--'title' is required, string, used when displaying results-->

* type: short-answer
* id: 1a3cc34f-ea21-4533-bed4-6da3c8c95a4e
* title: Example Short Answer Challenge

<!--'question' is required, markdown, the question to be answered-->

### !question

What will the following code produce?

```javascript
var myArray = ["Elie", "Janey", "Matt", "Parker", "Tim"];
myArray[3]
```

### !end-question

<!--'placeholder' is optional, the placeholder text in the input box. Removed when the user starts typing-->

#### !placeholder

What does myArray[3] equal?

#### !end-placeholder

<!--'answer' is required, the correct answer to the question.
By default, answers evaluated as case-insensitive exact match. If answer wrapped in '/', evaluated as regex. The answer to this question could have been defined as /\A['"]Parker['"]$/ to allow students to enter single or double quotes. Also supports regex ending in '/i' for case-insensitive regex. To test your regex, you can use http://rubular.com/-->

### !answer
"Parker"
### !end-answer

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Number

Number challenges allow a student to submit a number as the answer to a question. The answer is evaluated numerically, and the student can answer with a decimal or a fraction--so that things like 3/10, 30/100, .3, 0.3, 0.300 etc. are all equivalent. There also also an option when creating the challenge to define the precision used when the answer is scored -- see the code below for details.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'title' is required, string, used when displaying results-->
<!--'decimal' is optional, the number of decimal places that the answer will be rounded to before evaluating for correctness. If not specified, answer must be exact.-->

* type: number
* id: e88f0c35-7f2d-4990-81c1-a529d5e81dbb
* title: Example Number Challenge
* decimal: 5

<!--'question' is required, markdown, the question to be answered-->

### !question
Suppose a card is drawn from a standard 52 card deck. What's the probability that the card is a queen?
### !end-question

<!--'placeholder' is optional, the placeholder text in the input box. Removed when the user starts typing-->

#### !placeholder
Write your answer as a decimal to 5 places
#### !end-placeholder

<!--'answer' is required, the correct answer. Can be specified as a decimal like 0.07692 or a fraction like 1/13.-->

### !answer
1/13
### !end-answer

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Paragraph

Paragraph Challenges allow a student to submit a long free-form text answer to a question, such as a definition of explanation. The answers to these Challenges are not evaluated by Learn, but are available for the instructor to view.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'title' is required, string, used when displaying results-->

* type: paragraph
* id: f397a35a-2d2a-42e2-a8aa-9bc4be353e59
* title: Example Paragraph Challenge

<!--'question' is required, markdown, the question to be answered-->

### !question
Explain at least 2 benefits of writing semantic HTML.
### !end-question

<!--'placeholder' is optional, the placeholder text in the input box. Removed when the user starts typing-->

#### !placeholder
Write your answer here
#### !end-placeholder

<!--'explanation' is optional. Shown after the student correctly answers the question.-->

### !explanation
Your answer may have covered accessibility, SEO, and human readability.
### !end-explanation

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Javascript Code Snippet

Code Snippet Challenges allow a student to write code directly in Learn. The submission is evaluated against unit tests that are setup as part of the Challenge. The student then sees the standard output from the test runner in Learn.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'language' is required for type: code-snippet. For javascript, use 'javascript' -->
<!--'title' is required, string, used when displaying results-->

* type: code-snippet
* id: dd9c31af-0fe8-440d-b4ec-bab3e8dc8a1d
* language: javascript
* title: Javascript `Repeats` Function

<!--'question' is required, markdown, the question to be answered-->

### !question

## Repeats

Write a function named `repeats`
* `repeats` should take one argument, `str`, the string to test.
* For this exercise, you can assume that `str` is a string.
* If the first half of `str` equals the second half, return true.
* If `str` is an empty string, return true.
* Otherwise, return false.
* Do not use the `.repeat` method.

### !end-question

<!--'placeholder' is optional, the starting code in the editor. Not removed when the user starts typing-->

#### !placeholder

```js
function repeats(str) {
   // return str.substring(0, str.length/2) === str.substring(str.length/2, str.length);
}
```

#### !end-placeholder

<!--'tests' is required for code-snippets and contains the unit tests that will be run to evaluate the student submission. Tests should be broken down into as many 'it(should...)' blocks as possible, because this is how students will get results. -->

### !tests

```js
describe('repeats', function() {

    it("should return true when given an empty string (which seems strange, but go with it :) )", function() {
      expect(repeats(""), "Default value is incorrect").to.deep.eq(true)
    })

    it("should return true when the second half of the string equals the first", function() {
      expect(repeats("bahbah")).to.deep.eq(true)
      expect(repeats("nananananananana")).to.deep.eq(true)
    })

    it("should return false when the second half of the string does not equal the first", function() {
      expect(repeats("bahba")).to.deep.eq(false)
      expect(repeats("nananananann")).to.deep.eq(false)
    })

    it("should not use .repeat", function() {
      expect(repeats.toString()).to.not.match(/\.repeat/)
    })

})
```
### !end-tests

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Python Code Snippet

Code Snippet Challenges allow a student to write Python directly in Learn. The submission is evaluated against unit tests that are setup as part of the Challenge. The student then sees the standard output from the test runner in Learn.

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!-- type is required, type of challenge -->
<!--'language' is required for type: code-snippet. For python, options are 'python2.7' and 'python3.6' -->
<!-- id is required -->
<!-- title is required -->

* type: code-snippet
* language: python3.6
* id: 6f1a61d2-a3b4-402d-83be-38d443f03e72
* title: filter by class

<!-- !question is required -->

### !question

Implement the function `filter_by_class`: It takes a feature matrix, `X`, an array of classes, `y`, and a class label, `label`. It should return all of the rows from X whose label is the given label.

```python
>>> X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
>>> y = np.array(["a", "c", "a", "b"])
>>> filter_by_class(X, y, "a")
array([[1, 2, 3],
       [7, 8, 9]])
>>> filter_by_class(X, y, "b")
array([[10, 11, 12]])
```
### !end-question

<!-- !placeholder is optional, the starter code that will be added to the editor -->

### !placeholder

```python
def filter_by_class(X, y, label):
    '''
    INPUT: 2 dimensional numpy array, numpy array, object
    OUTPUT: 2 dimensional numpy array

    Return the rows from X whose corresponding label from y is the given label.
    '''
    # return X[y == label]
```
### !end-placeholder

 <!-- !tests are required -->

### !tests
```python
import unittest
import main as p		
import numpy as np

class TestChallenge(unittest.TestCase):
  def test_filter_by_class1(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "a")
      answer = np.array([[1, 2, 3], [7, 8, 9]])
      assert np.array_equal(result, answer)

  def test_filter_by_class2(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "b")
      answer = np.array([[10, 11, 12]])
      assert np.array_equal(result, answer)
```
### !end-tests

### !end-challenge

<!----------------------END CHALLENGE----------------------------->

<br><br>

## Java Code Snippet

tbd

<br><br>

## Project Challenge

Project Challenges allow a student to do work outside of Learn. After completing the work, the student submits a link (typically from Github) to the work that they did for tracking and review within Learn.

<!-- Let Learn run tests automatically on repo submissions! See [Testable Project Challenges](Testable-Project-Challenge.md).-->

<!----------------------BEGIN CHALLENGE----------------------------->

### !challenge

<!--'type' is required-->
<!--'id' is required, string, must be unique within a branch-->
<!--'title' is required, string, used when displaying results-->

* type: project
* id: 372d5f1f-e432-47f1-8de6-d0643f3773dc
* title: JS Native Array Methods

<!--'question' is required, markdown, the question to be answered-->

##### !question

### JS Native Array Methods

Submit the github repo containing your work on the js-native-array-methods below.

##### !end-question

<!--'placeholder' is optional, the placeholder text in the input field. -->

##### !placeholder

https://github.com/<username>/js-native-array-methods

##### !end-placeholder

### !end-challenge

<!----------------------END CHALLENGE----------------------------->



<br><br>

## Continue

Next: [04-cohort-setup.md](04-cohort-setup.md)
