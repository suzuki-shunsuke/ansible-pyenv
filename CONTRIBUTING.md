# Contributing

1. Fork (https://github.com/suzuki-shunsuke/ansible-pyenv/fork)
2. Clone the forked repository
3. Install npm dependencies
4. Create a feature branch
5. Make your change
6. Test
7. Commit your change
8. Rebase your local changes against the master branch
9. Create a new Pull Request

## Requirements

* [yarn](https://yarnpkg.com/lang/en/), npm: for commit message validation and Change Log generation
* [Vagrant](https://www.vagrantup.com/): for test

We use some node modules to validate commit messages and generate Change Log.

Install node modules by

```
$ yarn
```

or

```
$ npm i
```

In addition to [travis.ci](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv), we test at local with [Vagrant](https://www.vagrantup.com/).

## Test

In addition to [travis.ci](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv), we test at local with [Vagrant](https://www.vagrantup.com/).

```
$ cd tests
$ ansible-playbook --syntax-check test.yml
$ vagrant up --provision
```

## Commit Message Format

The commit message format of this project conforms to the [AngularJS Commit Message Format](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#commit-message-format).
By conforming its format, we can generate the [Change Log](CHANGELOG.md) and conform the [semantic versioning](http://semver.org/) automatically by [standard-version](https://www.npmjs.com/package/standard-version).
We validate the commit message with git's `commit-msg` hook using [validate-commit-msg](https://www.npmjs.com/package/validate-commit-msg) and [husky](https://www.npmjs.com/package/husky).

## Release

We generate the [Change Log](CHANGELOG.md) by [standard-version](https://www.npmjs.com/package/standard-version).
After merge your PR at the master branch,
The author ([suzuki-shunsuke](https://github.com/suzuki-shunsuke)) will generate the release tag.

```
$ npm run release
$ git push origin master --follow-tags
```
