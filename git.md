# git

## Rewrite the author's email for all commits

```bash
git filter-branch --env-filter 'export GIT_AUTHOR_EMAIL="foo@bar.baz"'
```

## Change the last commit author

```bash
git commit --amend --author 'Foo Bar <foo@bar.baz>'
```

## Setting email address for a single repository

```bash
git config user.email foo@bar.baz
```

## Cancel last local commit

```bash
git reset HEAD~1
```

## Revert changes on a file

```bash
git checkout path/to/file
```
