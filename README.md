# Quine Challenge

## Background

Willard van Orman Quine was a 20th century American Philosopher who influenced Douglas Hofstadter's fascinating work on the relationship between music, mathematics, and art.  Hofstadter's subsequent [book on the subject](http://search.ebscohost.com/login.aspx?direct=true&db=cat01619a&AN=up.655578&site=eds-live) in turn gives us the concept of _a quine_, which is:

 * A computer program whose purpose is to output its own source code.

For example, here is a purposefully simple _quine_ for Node.js.


```javascript
function f(f) {
  console.log(f.toString());
  console.log("f(f);");
}
f(f);
```

Seventy-six characters of self-replication.  We can shrink this down using a few techniques that should be familiar to most JS programmers.  This one-line version is just forty-three characters.

```javascript
f=() => console.log("f=" + f + ";f()");f()
```

It's possible to go shorter than this even, but the _quines_ get less readable and require significantly more cognitive investment, and our point here is to show the basic idea.  We leave these shorter node _quines_ for your future investigation because we have a different challenge for you…

## Task

We wish for you to attempt to write a web page whose output is its own source code: a _web-quine_.

We seek answers to the following questions:
1. What is the shortest _web-quine_?
2. What is the shortest _**valid** web-quine_?

### Rules
1. The page should be testable thus:
   1. Copy the quine output and save it to a file.
   2. Compare the output file with the source file: it should be a byte-for-byte replica of the source.
2. You may use HTML, CSS and JS as necessary.
3. All code must be part of a single self-replicating HTML file.
4. Check pages for validity using the [W3C's online validation service](https://validator.w3.org/#validate_by_input).  Warnings are permissible, but the document must contain no errors.

### Steps

#### Edit
1. Login to Github (you will need to register if you have not already).
1. **Fork** this repo (it's in the top right corner of [the repo page](https://github.com/portsoc/quine.git)).
2. Clone your fork of this repo using git:
```zsh
git clone https://github.com/<your_github_id>/quine.git
```
3. Edit `quine/index.html` until its output is the same as its source.
4. …then improve it.
5. …and come up with alternative (possibly better) solutions.

#### Share
1. Store your solutions in the `solutions` folder (we suggest your surname and the character length of the file in characters, similar to what we've done in the examples folder).
2. Commit your changes and push your repo back up to Github (regularly – release early, release often).
3. Send us a _Pull request_ through Github.
4. We will then incorporate your solutions into our repository.
