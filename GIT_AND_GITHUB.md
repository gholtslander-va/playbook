# Git & GitHub Conventions

These conventions apply to our open-source, internal and client projects.

## Basic Setup

A typical project in *Hyper* has a `master` branch, which always is production ready
and in some cases a `develop` branch when using a **Staging** server

## Commits

Write grammatically correct (i.e. start with a capital) commit messages in [imperative, present tense](http://stackoverflow.com/questions/3580013/should-i-use-past-or-present-tense-in-git-commit-messages).

Prefer concise commits over gigantic ones. When writing a concise commit message
is difficult, it may indicate too many unrelated changes.

## Branches

### Naming

Branches are awesome. We use `feature/`, `fix/` and `refactor/`:

```
feature/my-feature
fix/make-it-work
refactor/make-it-pretty
```

Use `--no-ff` when you merge to `master` or `develop`.

### Merging

It's okay to just push to `develop` or `master` if it's a quick fix and you really need
it out the door. Otherwise, make it a pull request.

#### Who merges the pull request?

Let's say you're working on a pull request. The tests are green and you're ready
to merge. Who does that? Basically anyone. Just not you.

#### Then what?

If you're working on an application and you merged to `develop` or `master`, you push it to
the staging or production server, respectively. The staging server should *always* be on the
tip of `develop` and the production server should *always* be on the tip of `master`.

If you're working on a gem and you merged to `master`, you may want to push a new
version. Or not.