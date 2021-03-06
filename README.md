#### Status
[![Build Status](https://travis-ci.org/piensa/piensa.github.io.svg?branch=blog-jekyll)](https://travis-ci.org/piensa/piensa.github.io)

### Installation

Follow this simple steps to run this project locally.
First let's check if you have **ruby** installed.

```sh
ruby --version
```

If you don't have Ruby installed, install [Ruby 2.0.0 or higher.](https://www.ruby-lang.org/en/downloads/)

Install Bundler. Make sure you have sudo or admin permissions.

```sh
gem install bundler
```

Go to the root of the project, where the `Gemfile` is. Then install all the required gems.

```sh
bundle install
```

Finally, run the Jekyll project locally

```sh
bundle exec jekyll serve
```
Preview your local Jekyll site in your web browser at http://localhost:4000.

If you need to see your drafts, just run this other command instead. Remember not to push files generated by this command in the `_site` folder.

```sh
bundle exec jekyll serve --drafts
```

For more information about Bundler, please read [Bundler's Purpose and Rationale.](http://bundler.io/rationale.html)

#### Running tests

In order to run tests locally, you should have [html-proofer](https://github.com/gjtorikian/html-proofer) installed. Just run this 2 commands, one for building the `_site` folder and the other for running tests locally in it.

```
bundle exec jekyll build
bundle exec htmlproofer ./_site --disable-external
```

After running the html_proofet if by any chance, you encounter with this error:
```
htmlproofer 3.0.6 | Error:  invalid byte sequence in US-ASCII
```

Run this commands on your console:
```
export LANG=en_US.UTF-8
export LANGUAGE=en_US.UTF-8
export LC_ALL=en_US.UTF-8
```

#### Making contributions

For making contributions, just make a fork of the `blog-jekyll` branch and send **all your push requests there.** The master branch will be updated by TRAVIS-CI.

#### Wiki Resources
* [How to create authors](https://github.com/piensa/piensa.github.io/wiki/How-to-create-authors)
* [How to create categories](https://github.com/piensa/piensa.github.io/wiki/How-to-create-categories)
