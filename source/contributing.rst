Contribution Guidelines
=======================

There are many ways to contribute to TopoToolbox from implementing new code or testing old code to writing documentation and showing off cool examples using TopoToolbox. We're really excited to see what you build with TopoToolbox!

We use git as a version control system and GitHub's Issues and Pull Requests to manage contributions to libtopotoolbox. Using git and GitHub effectively can take some practice. `The Turing Way's Git documentation <https://book.the-turing-way.org/reproducible-research/vcs/vcs-git>`_ and `GitHub's documentation <https://docs.github.com/en/get-started/start-your-journey/about-github-and-git>`_ are good resources to check out if you are new to this workflow or if you need a refresher.

You will need a GitHub account to contribute through Issues or Pull Requests. If you are unable to use GitHub, patches may also be [sent by email](https://git-send-email.io/) to william.kearney@uni-potsdam.de.

The TopoToolbox Organization
----------------------------

We have a `TopoToolbox organization <https://github.com/TopoToolbox>`_ on GitHub that hosts the development of TopoToolbox 3. This organization hosts many repositories (including the `website <https://github.com/TopoToolbox/topotoolbox.github.io>`_ you are reading right now), but if you would like to contribute new code with TopoToolbox, there are four key repositories to know about

* `topotoolbox3 <https://github.com/TopoToolbox/topotoolbox3>`_: The MATLAB implementation of TopoToolbox 3
* `pytopotoolbox <https://github.com/TopoToolbox/pytopotoolbox>`_: The Python implementation of TopoToolbox 3
* `topotoolboxr <https://github.com/TopoToolbox/topotoolboxr>`_: The R implementation of TopoToolbox 3
* `libtopotoolbox <https://github.com/TopoToolbox/libtopotoolbox>`_: The C library implementing shared functions for TopoToolbox 3

The other repositories are for testing (e.g. `snapshot_data <https://github.com/TopoToolbox/snapshot_data>`_) or documentation (e.g. `topotoolbox.github.io <https://github.com/TopoToolbox/topotoolbox.github.io>`_), and we have a few that implement additional functionality on top of the core TopoToolbox (e.g. `TTLEM <https://github.com/TopoToolbox/TTLEM>`_).

If you are working in a particular programming language (i.e. MATLAB, R or Python), you should probably check out the appropriate language-specific repository first. Documentation is split between this main website, the package repositories, each of which build their own language-specific documentation, and some additional repositories such as the `gallery <https://github.com/TopoToolbox/gallery>`_, which hosts examples of workflows using TopoToolbox.

You also don't have to contribute code to one of the official TopoToolbox repositories. You can also create your own repository under your name on GitHub (or any other code hosting plaform), using the dependency management tools of your programming language to depend on the core TopoToolbox code. This is a particularly good choice if you have built something that integrates TopoToolbox with other tools.

If you have your own repository that builds on TopoToolbox or if you have written articles or blog posts about TopoToolbox, we'd love to hear about it! Submitting a demo to the `gallery <https://github.com/TopoToolbox/gallery>`_ or posting on our `Discussions forum <https://github.com/orgs/TopoToolbox/discussions>`_ are great ways to share your work with the TopoToolbox community.

Each repository has some more specific guidelines for contributing to it, but the basic workflow using git and GitHub is the same for every repository.

Opening an issue
----------------

If you would like to report a bug or request a feature you can `create an issue <https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/creating-an-issue>`_ in the appropriate repository. Search the existing issues, including closed issues, to see if your problem has been discussed before.

If you are reporting a bug, please provide

- A full error message
- A minimal working example of code that triggers the error
- Details such as the operating system and the software you are using with TopoToolbox (e.g. the MATLAB release number or the Python version number or the C compiler used to build libtopotoolbox).

Contributing via pull requests
------------------------------

If you would like to contribute code, tests, or documentation to TopoToolbox, it is a good idea to first check the issue tracker of the particular repository you would like to contribute to. and discuss your contribution in a new or existing issue there. It is not necessary to get approval before making a contribution, but checking in can make sure that you aren't duplicating effort or implementing something that already exists but is poorly documented, for example.

Create your own `fork <https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo>`_ of the necessary repository. Once you have a fork, you can `clone <https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#cloning-your-forked-repository>`_ your fork of the repository to get the source code on your local computer.

The default branch of a TopoToolbox repository will usually be named ``main``. You are welcome to make your changes on the ``main`` branch, but this can lead to problems as the TopoToolbox repository diverges from your own. It can be easier to create a new branch for the changes you wish to make and commit changes to that branch. Running something like

.. code-block:: bash
		
   git checkout -b feature-name main

will create a new branch called ``feature-name`` starting at ``main``. Now make your changes to the code and save them. Commit them to the repository using

.. code-block:: bash
		
   git add file1 file2
   git commit

and then use ``git push origin feature-name`` to push your ``feature-name`` branch to GitHub.

Then `open a pull request <https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request>`_ to the TopoToolbox repository. One of the TopoToolbox maintainers will review your pull request and let you know if any changes need to be made before your contribution can be accepted. Changes can be pushed to your fork and will automatically show up in the pull request.

In most repositories,  a series of automated tests and formatting checks will run on your pull request, and GitHub will let you know if any of them fail.

Licensing
---------

TopoToolbox is an open source project licensed under the GNU Public License v3.0. Each repository should include a copy of the license and more details about copyright, etc. By making a contribution to TopoToolbox, you are certifying that you have the right to submit it under the GPLv3.
