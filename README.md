npm-janitor
===========

janitor is coming soon.

----
# The idea:

Create a bot that would:

* Go throught all the published node modules for a partiuclar user.
* Check for validity of their package.json
* Raise an issue or send a PR as the user itself not as a bot!

---

# The New strategy:
 
 * Get write acess to repos of the user using [this](https://npm-janitor.herokuapp.com/login).
 
 * Using `package-json-validator` module validate the `package.json`
 
 * Send a PR if needed. 


# The Old strategy:

* Fix all published node module names from the [regsitry](https://registry.npmjs.org/-/all/) we might use `jsonselect` module to filer out names.

* Iterate over the names using `npm` module get the `package.json`

* Using `package-json-validator` module validate the `package.json`

* If any issues found with the `package.json` clone the repo.

* Create an issue and send a PR if possible fixing the `package.json` using `npm` module.

---

<strike># Project on halt!</strike>

I contacted a human from Github and got the below as a reponse, so until we get a green signal, this seems to be a rest :/

```
Hi Hemanth,

Thanks for getting in touch! The problem is this item:

> Raise an issue or fork and send a PR

We don't currently allow bots to create issues, comments, and PRs. This usually ends up in repo owners reporting these things as spam.

Let us know if you have any other questions!

Cheers,
Jamie
```

P.S: WIP now!
 
