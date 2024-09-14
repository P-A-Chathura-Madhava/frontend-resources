# Semantic Versioning (semver)

- [Versioning best practices](https://cpl.thalesgroup.com/software-monetization/software-versioning-basics)

> We will be using `changeset` library to implement versioning in our apps—it supports both monorepos & standalone apps.

---

## Setup changeset

- Install the changeset library in your app by running `npm install @changesets/cli`
- Initialize changeset in your app by running `npx changeset init` (This will create a `.changeset` directory in your app's root directory, where you can store your versioning and release notes.)
- Before creating a PR, use `npx changeset` command to genrate a new changeset file
- Once the PR is approved, you can run `npx changeset version` command to bump up the version number in your `package.json` (Later, this part can be automated using github actions)

> You can also configure [changeset-bot](https://github.com/apps/changeset-bot) so that it can validate your PR

## Automating version bump

- Checkout to `develop` branch
- Create `.github/workflows` directory
- Copy the `release.yml` file inside `resources/.github/workflows` directory & push the change to `origin`

> You can refer to [changeset docs](https://github.com/changesets/action) to understand the release.yml

### Workflow permissions

For this action to run properly, you should update `Workflow permissions` in your repo.

Settings -> Actions [General] -> Workflow permissions

```
[x] Read and Write permissions


[x] Allow Github Actions to create and approve pull requests
```
