<img src="images/logo.png" height=72>

# Digital Medicines Documentation #

This is the template repository for documentation projects used in the Digital Medicines portfolio. It is designed primarily for use in developing specifications, but is suitable for other documentation types.

## Creating a New Documentation Project ##

### Setting up a repository from the template ###

To create a new project from the template we're going to clone the template repository, remove all its history and then set up a new repository using the same files:

  0. Create a new empty repository on Github to hold the new documentation.
      - Go to https://github.com/NHSEPS
      - Click on *New repository* and set name & description to sensible values - we'll assume it's called `new-spec-repository` here
  1. Clone the template repository to a local directory, with minimal history.
```shell
git clone --depth 1 https://github.com/NHSEPS/documentation-template.git new-spec-repository
```
  2. Delete the .git directory which holds history and initialize a new repository with no history before adding & committing files to the new repository.
```shell
cd new-spec-repository
rm -rf .git
git init
git add .
git commit -m "Initial commit on new documentation"
```
  3. Tell git where to push and fetch files to, then push them
```shell
git remote add origin https://github.com/NHSEPS/new-spec-repository.git
git push -u origin master
```
  4. Done

## Building the specification

To build the documentation locally

- Install [Ruby](https://www.ruby-lang.org/en/documentation/installation/#homebrew)
- Install Jekyll
  - Install [Jekyll](https://jekyllrb.com/docs/installation/) for OS X/Linux
  - Install [Jekyll](https://jekyllrb.com/docs/windows/) for Windows
- Navigate to your project directory and run: `bundle install`
- Now run Jekyll: `bundle exec jekyll serve`
- Browse website [Browser](http://localhost:4005): `http://localhost:4005`

### Troubleshooting

1) Fix warnings related to SSL certificate checking (by configuring the SSL_CERT_FILE env variable) by following instructions to [download and reference a cacert.pem file](https://gist.github.com/fnichol/867550).

2) Fix warnings related to the Jekyll GitHub Metadata plugin, by [configuring the JEKYLL_GITHUB_TOKEN environment variable](https://github.com/jekyll/github-metadata).

### Generating a Release ###

<mark>TODO</mark>

## Reviewing Documentation ##

Often for more formal documentation like specifications formal review cycles may be required.

### Issue Tracker ###

The Github issue tracker can be used to track comments and issues on the documentation.

## Branching Model ##
