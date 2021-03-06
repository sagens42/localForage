# Filing issues

Please make sure your issue hasn't been addressed already and it is not in the
list of likely-to-be-rejected features below. If you have a bug to report,
please file it. If you'd like to see a feature implemented, you can file an
issue, but know that pull requests for small things like adding a line in a
config file will get more attention than an issue asking someone else to do it.

# Contributing to localForage

First off: thanks! Open source software (and thus all software) exists because
of people like you. <3

If you'd like to contribute to localForage, it's as simple as opening a pull
request on GitHub. After that someone will code review your work and either
ask you to fix any errors or merge the code into master. Here are a few tips:

* **do your work on a feature branch**: this keeps things clean and easy
* **try to rebase master into your branch**: this keeps the commit history clean and avoids merge commits inside feature branches
* **write tests**: if you're adding new features, _please_ write tests; likewise, if you're fixing a bug that wasn't previously caught by a test, please add one
* **run `make` before you commit**: this will build out the files in the `dist/` folder and ensure your tests pass

Please commit changes inside the `dist/` folder along with your changes in the
`src/` folder--**do not make these changes separate commits**.

If you have any questions, need some help, or anything else, don't feel shy!
The team behind this library is often available on IRC
([irc.mozilla.org](https://wiki.mozilla.org/IRC) on the `#apps` channel).

## Features localForage will reject

### node.js support

localForage is a browser library with a specific focus on client-side,
offline storage. It is not a general-purpose storage library and is not meant
to allow for the same API on the client and the server. Implementing the
localForage API wouldn't be hard (it's just localStorage with callbacks and
ES6 promises), but it's a job for another library.

### Legacy browser support

Basically this means anything before IE 8. I know there are hacky ways to
support storage with cookies or IE Userdata or whatever, but anything worse
than localStorage isn't worth investing into.
