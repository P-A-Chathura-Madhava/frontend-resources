# PR (Pull Request) Guide

You could add a pr template to your `default` branch in your repo so that everytime you create a new pr, the description will be automatically filled!

> You should fill out the missing details in the template each time you open a PR

## Add PR Template

- Checkout to your `default` branch
- Create a folder named `.github` in your root foolder
- Copy the `pull_request_template.md` file inside `resources/.github/` directory & push the change to `origin`

> You could change your `default` branch to `develop` if needed—refer to this [doc](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/changing-the-default-branch)

## Branch Protection Rules

Make sure to add a protection rule to both `main` & `develop` branches as below:

Settings -> Branches -> Add branch protection rule

```
[x] Require a pull request before merging
    [x] Require approvals
    [x] Dismiss stale pull request approvals when new commits are pushed
[x] Require conversation resolution before merging
```
