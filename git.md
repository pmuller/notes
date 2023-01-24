# git

## Include another git repository with its history

```bash
REMOTE_NAME=foo
REMOTE_URL_OR_LOCAL_PATH=/path/to/repository
TARGET_BRANCH=feature/integration-$REMOTE_NAME-repository
INTEGRATION_BRANCH=$TARGET_BRANCH-integration
# Add remote repository
git remote add $REMOTE_NAME $REMOTE_URL_OR_LOCAL_PATH
# Fetch content of remote repository
git fetch $REMOTE_NAME
# Checkout our source branch from the remote repository
git checkout $REMOTE_NAME/$REMOTE_BRANCH
# Create an integration branch
git checkout -b $INTEGRATION_BRANCH
# Do your and commit your changes.
# Usually this involves moving all the imported repository content to a specific
# prefix, in order avoid merge conflicts.
# Then merge the integration branch into your target branch
git checkout $TARGET_BRANCH
git merge $INTEGRATION_BRANCH --allow-unrelated-histories
```

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
