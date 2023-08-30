# Doc Store

## Before the interview

There's **_no need to do any work in advance_** beyond reading through the question, and setting up a project in your preferred language and editor, or a [repl.it](https://docs.replit.com/getting-started/intro-replit) if you'd prefer to code in the browser.

We'll be pairing with you on the problem during the interview, so there'll be lots of time for questions and discussion, and you're free to google things as you go just like you would in a real project. 

## The Problem

You've been asked to build a simple datastore for a new project. The datastore will be used to store documents of different types, each with different metadata.

### Part One

Given a series of documents, each with a `type` and `body`, implement a simple datastore that can retrieve all documents of a given type:

| Type    | Body                    |
|---------|-------------------------|
| recipe  | how to make scones      |
| recipe  | mars bar tarte tartin   |
| article | 10 ways to write a list |
| recipe  | the eggless omlette     |

e.g: `fetch("recipe")` should return all three recipe documents:

| Type   | Body                  |
|--------|-----------------------|
| recipe | how to make scones    |
| recipe | mars bar tarte tartin |
| recipe | the eggless omlette   |

### Part Two

Documents have other metadata, e.g. `recipe` documents have a `vegan?` flag, `article` documents have a `site`, etc.

| Type    | Vegan? | Site    | Body                    |
|---------|--------|---------|-------------------------|
| recipe  | no     | -       | how to make scones      |
| recipe  | no     | -       | mars bar tarte tartin   |
| article | -      | Listify | 10 ways to write a list |
| recipe  | yes    | -       | the eggless omlette     |

Update the datastore to so that documents can be added along with the new metadata, then allow documents to be retrieved by any metadata property.

e.g. `fetch(type: "recipe", vegan?: "yes")` should return the eggless omlette recipe:

| Type    | Vegan? | Site    | Body                    |
|---------|--------|---------|-------------------------|
| recipe  | yes    | -       | the eggless omlette     |

e.g. `fetch(site: "Listify")` should return the article:

| Type    | Vegan? | Site    | Body                    |
|---------|--------|---------|-------------------------|
| article | -      | Listify | 10 ways to write a list |

### Part Three

Discuss the trade-offs of the datastore you've built.
- What are the advantages and disadvantages of the approach you've taken?
- What would you do differently if you had more time?
- What would you do differently if you had to support 1000x more documents?
- What would you do differently if you had to support 1000x more metadata properties?


