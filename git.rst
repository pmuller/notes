git
===

* Rewrite the author's email for all commits:

    .. code-block:: console

        $ git filter-branch --env-filter \
            'export GIT_AUTHOR_EMAIL="foo@bar.baz"'

* Change the last commit author:

  
    .. code-block:: console

        $ git commit --amend --author 'Foo Bar <foo@bar.baz>'

* Setting email address for a single repository:

    .. code-block:: console

        $ git config user.email foo@bar.baz

* Cancel last local commit:

    .. code-block:: console

        $ git reset HEAD~1

* Revert changes on a file:

    .. code-block:: console

        $ git checkout path/to/file
