# Git Resources

- [Git cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Git commit best practices](https://chiamakaikeanyi.dev/how-to-write-good-git-commit-messages/)
- [Git commit types](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow-1709)

> Note: Download Git Graph extension in VSCode

---

## Git Branch Strategy

- `main` & `develop` branches should always be ready to deploy into `prod` & `dev` environments—avoid working on these branches!

- Each new `task` should have its own branch based on task type—tasks should be merged into `develop` through a PR once done!

- Merging `develop` into `main` should only be done after QA testing is finished!

### Possible branch names

```
- main
- develop
     |__ feature/FeatureName
     |__ feature/[ticket-number]/FeatureName
     |__ fix/[bug-number]/BugName
     |__ ...
```

> First part of the branch will be a commit-type which will depend on the task assigend to you
