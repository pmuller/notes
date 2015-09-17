git
===

* Rewrite the author's email for all commits:

  .. code-block:: console

      $ git filter-branch --env-filter \
          'export GIT_AUTHOR_EMAIL="philippe.muller@gmail.com"'
