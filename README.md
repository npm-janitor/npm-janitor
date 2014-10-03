npm-janitor
===========

janitor is coming soon.

----
# The idea:

Create a bot that would:

* Go throught all the published node modules.
* Check for validity of their package.json
* Raise an issue or fork and send a PR

---

# The strategy:

* Fix all published node module names from the [regsitry](https://registry.npmjs.org/-/all/) we might use `jsonselect` module to filer out names.

* Iterate over the names using `npm` module get the `package.json`

* Using `package-json-validator` module validate the `package.json`

* If any issues found with the `package.json` clone the repo.

* Create an issue and send a PR if possible fixing the `package.json` using `npm` module. 