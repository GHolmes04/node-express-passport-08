#Express authentication
In this lesson, we'll be building an express application with user
authentication.

##Objectives
After this lesson, students will be able to:
- ... add user authentication to an express application
- ... set up a local authentication strategy with Passport.js

##Setup
Before we can do anything, we need to install our dependencies:

```bash
$ npm install
$ npm install passport --save
$ npm install passport-local --save
$ npm install bcrypt --save
```

###What are those modules for?
Passport is the core module for authentication here. It is organized in
a modular manner, not tied to any particular style of authentication, instead
importing strategy modules. Passport is capable of everything from standard
username-and-password (local) authentication to authentication with Google,
Facebook, or other social networking sites using the OAuth protocol, and
beyond.

`passport-local` is a local strategy for passport, which we are using for
simplicity. With this strategy, we will be storing and retrieving user
credentials in our very own databases, and hashing our own passwords for
secure storage.

`bcrypt` is a key derivation function designed to be arbitrarily slow. Its
purpose is to take a low-entropy (not very random) input, such as a password,
and produce a high-entropy output suitable for use as an encryption key. We
will use it to hash our passwords for secure storage.

##Code-along
We'll be doing this as a code-along, where I will make periodic commits to
the **solved** branch of this repository. You will be able to follow my commits
on that branch to review this material in the future.

###lib/passport.js
Create the file and directory, then proceed.

We will be using this file to configure `passport`. You will be provided an
initial state of comments stating what needs to be done.

