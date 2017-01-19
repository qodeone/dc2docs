Developing
==========

Choosing an issue
-----------------

| Commerce uses GitHub for code and drupal.org for tracking issues.
| To choose an issue, go through `the open issues`_, pick one you like
  and **assign it to you**.

| If you need help choosing an issue or working on one, join the
  Commerce 2.x office hours.
| They are held every wednesday at 3PM GMT+1 on the *#drupal-commerce*
  `IRC channel`_.

\*\*\ Tip:** You can also view the issue queue as a `kanban board`_.

Creating a pull request
-----------------------

| Start by creating a branch for your work.
| The branch name should contain a brief summary of its id and the
  issue, e.g **2276369-fix-product-form-notice**:

::

    cd web/modules/contrib/commerce
    git checkout -b 2276369-fix-product-form-notice

Once you’re done with development, push your commits to your fork:

::

    git commit -a -m "Issue 2276369: Fix notice in the product form."
    git push fork 2276369-fix-product-form-notice

| You can now go to your fork’s GitHub page and `create a pull
  request`_.
| Your pull request should link to the drupal.org issue, and vice-versa.

After your code has been reviewed, you might be asked to perform some
changes and then have them reviewed again:

::

    # Change the desired files.
    git commit -a -m "Addressed feedback."
    git push fork 2276369-fix-product-form-notice

Updating the branch will automatically update the related pull request.

Keeping up to date
------------------

| Your forked repository and the original one (called *origin*) will
  eventually get out of sync.
| Periodically update your fork by doing:

::

    # Update your local branch.
    git checkout 8.x-2.x
    git pull origin/8.x-2.x
    # Push the update to your GitHub fork.
    git push fork 8.x-2.x

| Your pull request might also need rebasing, to re-apply your changes
  on top of the latest code.
| Once you’ve updated the master branch (8.x-2.x), rebase your branch:

::

    git checkout 2276369-fix-product-form-notice
    git rebase 8.x-2.x
    git push -f fork 2276369-fix-product-form-notice

That’s it! Happy contributing!

.. _the open issues: https://www.drupal.org/project/issues/search/commerce?assigned=&submitted=&project_issue_followers=&status%5B0%5D=Open&version%5B0%5D=8.x&issue_tags_op=%3D&issue_tags=&text=&&&&order=field_issue_priority&sort=desc
.. _IRC channel: https://www.drupal.org/irc
.. _kanban board: https://contribkanban.com/board/commerce2x
.. _create a pull request: https://help.github.com/articles/using-pull-requests#initiating-the-pull-request
