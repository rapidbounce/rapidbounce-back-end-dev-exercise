# Back-End Developer Exercise

This is the exercise for the Back-End part of our position at rapidbounce. The objective of this exercise is to create a web application.

## Effort

You should spend **no more than 4 hours** working on this exercise. We will by no means police you, but we do trust you to respect and comply with this constraint.

## Spec

This is the functionality of the web application we expect you to create. It should include an HTML page and an API endpoint.

### Home page (`/`)

- This is the page the user sees, when they open the web application
- This page contains a form with:
  - A text area
  - A submit button
  - An empty div element for results
- When the form is submitted:
  - The submit button should be disabled and it's text should be set to `Loading...`.
  - The value text area should be submitted to the `/api/sort/` endpoint as a JSON list (each line in the text area corresponds to a JSON list element).
- When the API endpoint responds:
  - The button should be enabled again, with the original text.
  - The sorted results should be displayed the div element for the results.

### Sorting API endpoint (`/api/sort/`)

- This endpoint should receive and array of strings, sort them and return them back
- The sorting algorithm should be [Quicksort](https://en.wikipedia.org/wiki/Quicksort) (do not use any libraries or built-in functions for sorting)
- The API endpoint should validate that the correct data (array of strings) has been submitted, otherwise it should return a 400 status code

## Documentation

Your submission should be brief, yet clearly documented. In particular:

- **README**: The current README file should be replaced with one containing information only about what this web application does and how to run it.
- **Code**: Each function you write should be documented about what it does and how it works.

## Example

If the user enters the text below:

```
banana
apple
orange
```

The following JSON request should be made:

```
POST /api/sort/

[
    "banana",
    "apple",
    "orange"
]
```

The following JSON response should be returned:

```
[
    "apple",
    "banana",
    "orange"
]
```

And the following text should be displayed when the request completes:

```
apple
banana
orange
```

## Submission process

Please follow the steps below, in order to submit the exercise

1. [Create a new **private** repository using this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).
2. Add [@1qk1](https://github.com/1qk1) as a collaborator.
3. [Create a new branch for your implementation](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
4. Implement the exercise in your new branch.
5. [Create a Pull Request with your implementation](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) and add [@1qk1](https://github.com/1qk1) [as a reviewer](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).
