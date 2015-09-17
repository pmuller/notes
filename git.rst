git
===

* Rewrite the author's email for all commits:

    .. code-block:: console

        $ git filter-branch --env-filter \
            'export GIT_AUTHOR_EMAIL="foo@bar.baz"'

* Change the last commit author:

  
    .. code-block:: console

        $ git commit --amend --author 'Foo Bar <foo@bar.baz>'

