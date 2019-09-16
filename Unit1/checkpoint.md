# Checkpoint

This is a checkpoint, which is an end-unit assessment.

This example includes 3 questions -- a multiple choice question, a short answer question, and a javascript code snippet question.

<!--BEGIN CHALLENGE-->

### !challenge

* type: multiple-choice
* id: 436df042-671f-4609-8fcd-6a59e2c6d5f6
* title: Multiple Choice Example
* points: 3

##### !question

Galvanize teaches courses in which of the following?

##### !end-question

##### !options

* Software Engineering
* User Experience Design
* Sales Strategy

##### !end-options

##### !answer

Software Engineering

##### !end-answer

##### !explanation

##### !end-explanation

### !end-challenge

<!--END CHALLENGE-->

<!--BEGIN CHALLENGE-->

### !challenge

* type: short-answer
* id: 5dc57094-3c36-4447-aa68-d8721375bc84
* title: Short Answer Example

##### !question

What is the unix command to change directories?

##### !end-question

##### !answer

/cd/

##### !end-answer

##### !placeholder

Your Answer

##### !end-placeholder

##### !explanation

##### !end-explanation

### !end-challenge

<!--END CHALLENGE-->

<!--BEGIN CHALLENGE-->

### !challenge

* type: code-snippet
* language: javascript
* id: 15a618dd-9553-4d50-8420-c4e09d36e7ba
* title: Javascript Snippet Example

### !question

Write a function that returns the sum of two numbers.

### !end-question

### !placeholder

```js
 function addTwoNumbers(num1, num2) {
   // Uncomment the next line so that this function returns the sum of num1 and num2
   // return num1 + num2
}
```

### !end-placeholder

### !tests

```js

describe('addTwoNumbers', function() {

    it("adds 2 positive numbers", function() {
      expect(addTwoNumbers(1,2), "Error message").to.deep.eq(3)
    })
    
    it("adds 2 negative numbers", function() {
      expect(addTwoNumbers(-3,-4), "Error message").to.deep.eq(-7)
    })
})

```

### !end-tests

### !explanation

### !end-explanation

### !end-challenge

<!--END CHALLENGE-->
