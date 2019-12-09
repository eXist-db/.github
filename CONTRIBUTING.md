# Contributing to eXist-db
We welcome all contributions to eXist-db!

We strongly suggest that you join the [eXist-development mailing](https://lists.sourceforge.net/lists/listinfo/exist-development "eXist Development Mailing List") list and also subscribe to the [eXist-commits mailing list](https://lists.sourceforge.net/lists/listinfo/exist-commits "eXist SCM Commits Mailing List"), so that you can collaborate with the eXist team and be kept up to date with changes to the codebase.

## General Issues
If you wish to contribute, the general approach is:

-   Fork the repo on GitHub
-   `git clone` your fork
-   Do your stuff! :-)
-   Commit to your repo. We like small, atomic commits that don't mix concerns.
-   Make sure your branch is based on the latest eXist-db `develop` or `master` branch before making a pull-request. This will ensure that we can easily merge in your changes. See [Syncing a Fork](#syncing-a-fork).
-   Push your hotfix or feature branch to your GitHub using GitFlow: `git flow feature publish my-feature`.
-   Send us a Pull Request on GitHub from your branch to our `develop` branch.
-   Once the Pull Request is merged you can delete your branch, you need not finish or merge it, you will however want to sync your develop branch to bring back your changes. See [Syncing a Fork](#syncing-a-fork).

Pull Requests are reviewed and tested before they're merged by the respective development team.
However, we have one golden rule, even within the core team: **never merge your own pull request**. This simple-but-important rule ensures that at least two people have considered the change.

Although the following are taken from our [Developer Manifesto](http://www.exist-db.org/exist/apps/doc/devguide_manifesto.xml "eXist Project Developer Manifesto") and [Code Review Guide](http://www.exist-db.org/exist/apps/doc/devguide_codereview.xml "eXist Project Code Review Guide"), the main things that get a Pull Request accepted are:

-   **Only change what you need to.** If you must reformat code, keep it in a separate commit to any syntax or functionality changes.
-   **Test.** If you fix something prove it, write a test that illustrates the issue before you fix the issue and validate the test. If you add a new feature it needs tests, so that we can understand its intent and try to avoid regressions in future as much as possible.
-   **Make sure the appropriate licence header appears at the top of your source code file.** We mostly use [LGPL v2.1](http://opensource.org/licenses/LGPL-2.1 "The GNU Lesser General Public License, version 2.1") for eXist and *strongly* encourage that, but ultimately any compatible [OSI approved license](http://opensource.org/licenses "Open Source Licenses") without further restrictions may be used.
-   **Run existing tests.** We don't accept code that causes regressions.
