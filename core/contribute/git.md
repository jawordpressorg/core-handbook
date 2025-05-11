<!--
# The Code Repository (Git)
-->

<<<<<<< HEAD
Contributors to WordPress may submit patches created via either **Git** or **[SVN](https://make.wordpress.org/core/handbook/contribute/svn/)**. This documentation focuses on the **Git** option.
=======
# コードリポジトリ (Git)
>>>>>>> main

<!--
Contributors to WordPress may submit patches created via either **Git** or **[SVN](https://make.wordpress.org/core/handbook/contribute/svn/)**. This documentation focuses on the **Git** option.
-->

\[alert\]WordPress の貢献者は、**Git** または [SVN](https://ja.wordpress.org/team/handbook/core/contribute/svn/) で作成したパッチを提出できます。このドキュメントは、**Git** オプションにフォーカスしています。\[/alert\]

<!--
## Summary
-->

## 概要

<!--
[Git](https://git-scm.com/) is a distributed version control system originally created by Linus Torvalds to assist with the management of the Linux kernel.
-->

[Git](https://git-scm.com/) は、もともと Linus Torvalds が Linux カーネルの管理を支援するために作成した分散型バージョン管理システムです。

<!--
The canonical WordPress repository is managed using Subversion. To better support developers who are more comfortable working with Git, official, up-to-date Git mirrors of the WordPress repository are available at `git://develop.git.wordpress.org/` and `https://github.com/WordPress/wordpress-develop`.
-->

WordPress の標準的なリポジトリは Subversion で管理されています。Git を使い慣れた開発者をサポートするために、公式で最新の WordPress リポジトリ Git ミラーは `git://develop.wordpress.org/` と `https://github.com/WordPress/wordpress-develop` で利用できます。

<!--
**Please note:** while many people find it easier to use `git` to manage their patches, pull requests submitted to GitHub will not be merged there. Patches can be created and reviewed in GitHub pull requests, but they **must** be associated with a Trac ticket. To better understand what this means, see the [GitHub Pull Requests for Code Review page](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/).
-->

**注意してください:** 多くの人は、パッチの管理に `git` を使うほうが簡単だと考えていますが、GitHub に提出されたプルリクエストはマージされません。パッチは GitHub のプルリクエストで作成・レビューできますが、**必ず** Trac チケットと関連付けられている必要があります。この意味をよりよく理解するために、[コードレビューのための GitHub プルリクエストのページ](https://ja.wordpress.org/team/handbook/core/contribute/git/github-pull-requests-for-code-review/)を参照してください。

<!--
## Repository Structure
-->

## リポジトリの構造

<!--
The WordPress Git mirror contains a complete history of the codebase. Each Subversion commit is represented by a Git changeset. Use the `git log` utility to browse the history of the project. The layout of the repository is as follows:
-->

<<<<<<< HEAD
=======
WordPress の Git ミラーは、コードベースの完全な履歴を含んでいます。Subversion の各コミットは、Git のチェンジセットで示されています。プロジェクトの履歴を見るには、`git log` ユーティリティを使います。リポジトリのレイアウトは次のとおりです。

<!--
>>>>>>> main
*   The **trunk** branch, which corresponds to SVN **trunk**. This is the bleeding-edge branch, containing the alpha version of the next major release. Except in special cases, contributors should prepare their patches against the trunk branch.
*   A branch exists corresponding to each major release series, named using the first two digits of versions in that series. For example, 4.5.1 was released from the `4.5` branch. Use `git branch -r` to view a complete list of branches in the remote repository, and use commands like `git checkout -b 4.5.x origin/4.5` to create local branches that track remote branches.
*   All WP releases (starting with 1.5.0) are represented by Git tags. Use `git tag` to see the list.
-->

*   SVN の **trunk** に相当する **trunk** ブランチです。これは最先端のブランチで、次のメジャーリリースのアルファ版を含んでいます。特別な場合を除き、貢献者は trunk ブランチに対してパッチを準備すべきです。
*   各メジャーリリースシリーズに対応するブランチが存在し、そのシリーズのバージョンの最初の2桁の数字を使って名前が付けられています。たとえば、4.5.1は `4.5` ブランチからリリースされています。
*   WP のすべてのリリース (1.5.0以降) は Git タグで表されています。一覧を見るには `git tag` を使ってください。

<!--
## Patches
-->

## パッチ

<!--
Suggested improvements and bugfixes for WordPress should be submitted as **patches**. A [patch](https://make.wordpress.org/core/glossary/#patch) is a special text file that describes changes to code, by identifying the files and lines which are added, removed, and altered. It may also be referred to as a **diff** (after the Unix command to generate a differences file). Patches have the extension of either `.patch` or `.diff`. Patch files can then be submitted for consideration to [WordPress Trac](https://core.trac.wordpress.org/), the project’s official bugtracker.
-->

WordPress の改善やバグフィックスの提案は、**パッチ** として提出する必要があります。[パッチ](https://make.wordpress.org/core/glossary/#patch)とは、コードの変更点を記述した特別なテキストファイルのことで、追加、削除、変更されたファイルや行を特定できます。これは、(差分ファイルを生成する UNIX コマンドにちなんで) **diff** とも呼ばれます。パッチは `.patch` または `.diff` という拡張子を持っています。パッチファイルは、プロジェクトの公式バグトラッカーである [WordPress Trac](https://core.trac.wordpress.org/) に提出できます。

<!--
Using the `git` cli client, you can create a patch file as follows:
-->

`git` クライアントを使って、以下のようにパッチファイルを作成できます。

<!--
1.  Clone the repository to your local machine: `$ git clone git://develop.git.wordpress.org/ /path/to/wordpress-develop`
2.  Create a working branch (it’s better not to modify `trunk` because this should always be the latest version of the official code). To keep your local checkout organized, it’s suggested that you use the Trac ticket number as part of your branch name, eg: `$ git checkout -b 30000-add-more-alots   `
3.  Make your modifications to the codebase. Stage the changes (`git add`), and commit (`git commit`).  [The official git documentation](https://git-scm.com/docs/gittutorial) includes a tutorial on this.
4.  Use `git diff` to review the differences between your local branch and the trunk branch: `$ git diff trunk 30000-add-more-alots` †
5.  Once you’re ready to submit your patch to Trac, generate a patch file using `git diff`, specifying that the output should be saved in a `.diff` file. In general, the file name should be the ticket number you are working on with `.diff` as the extension (or `.2.diff`, `.3.diff`, etc. if there are already patches on the ticket). Example command: `$ git diff trunk 30000-add-more-alots > 30000.diff`
6.  Upload the patch to the appropriate Trac ticket.
-->

1.  リポジトリをローカルマシンにクローンします: `$ git clone git://develop.git.wordpress.org/ /path/to/wordpress-develop`
2.  作業用ブランチを作成します (`trunk` は常に公式コードの最新バージョンであるべきですので、変更しないほうが良いでしょう)。ローカルでのチェックアウトを整理するために、ブランチ名の一部として Trac チケット番号を使用することを推奨します。例: `$ git checkout -b 30000-add-more-alots `
3.  コードベースに変更を加えます。変更をステージ (`git add`) して、コミット (`git commit`) してください。[公式の git ドキュメント](https://git-scm.com/docs/gittutorial)には、これに関するチュートリアルがあります。
4.  ローカルブランチと trunk ブランチの差分を確認するには、`git diff` を使用します: `$ git diff trunk 30000-add-more-alots` (脚注)
5.  Trac にパッチを提出する準備ができたら、`git diff` を使用してパッチファイルを生成しますが、`.diff` ファイルとして保存するように指定します。一般的に、ファイル名はあなたが作業しているチケット番号で、拡張子は `.diff` にしてください (すでにパッチがあるチケットでは `.2.diff` や `.3.diff` などになります)。コマンドの例: `$ git diff trunk 30000-add-more-alots > 30000.diff`
6.  パッチを適切な Trac チケットにアップロードしてください。

<!--
### Unit Tests
-->

### ユニットテスト

<!--
We strongly recommend [running the PHPUnit test suite](https://make.wordpress.org/core/handbook/testing/automated-testing/phpunit/) (and writing unit tests for your patch) before submitting it to Trac. This makes it many times easier for committers to review and commit your changes.
-->

Trac に投稿する前に [PHPUnit テストスイート](https://ja.wordpress.org/team/handbook/core/testing/automated-testing/phpunit/)を実行すること (そしてパッチのユニットテストを書くこと) を強く推奨します。それにより、コミッターがあなたの変更をレビューし、コミットすることが何倍も簡単になります。

<!--
When downloading the repository from `git`, a few of the PHPUnit tests related to the importer plugin will fail because the `tests/phpunit/data/plugins/wordpress-importer` directory is not contained in the `git` repositories. Here’s how to fix that:
-->

`git` からリポジトリをダウンロードすると、importer プラグインに関連するいくつかの PHPUnit テストが失敗します。これを修正する方法は次のとおりです。これは `tests/phpunit/data/plugins/wordpress-importer` ディレクトリが `git` リポジトリに含まれていないことが原因です。

```
cd /path/to/wordpress-develop
cd tests/phpunit/data/plugins/
svn co \
    https://plugins.svn.wordpress.org/wordpress-importer/trunk/ \
    wordpress-importer
```

<!--
### Usage Notes for Git
-->

<<<<<<< HEAD
† If your `trunk` branch has changed since you last worked on your patch (for example, if you’ve pulled down the latest code), you’ll need to [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) your branch against the latest code. This is a great way to keep your patches up to date, and it’s much easier with Git than with svn. Here is an example sequence of commands to update your `trunk` branch then refresh your patch on top of the latest code (make sure you have [no uncommitted changes in your repository](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) first):
=======
### Git を使用するときの注意点

<!--
† If your `trunk` branch has changed since you last worked on your patch (for example, if you’ve pulled down the latest code), you’ll need to [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) your branch against the latest code. This is a great way to keep your patches up to date, and it’s much easier with Git than with svn. Here is an example sequence of commands to update your `trunk` branch then refresh your patch on top of the latest code (make sure you have [no uncommitted changes in your repository](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) first):
-->

脚注: 前回パッチを作成したときから `trunk` ブランチが変更された場合 (たとえば最新のコードを取り込んだ場合)、最新のコードに対してブランチの [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) を行う必要があります。これは、パッチを最新の状態に保つためのすばらしい方法であり、svn よりも Git の方がずっと簡単です。以下は、`trunk` ブランチを更新してパッチを最新のコードに更新するためのコマンドの例です (最初に[あなたのリポジトリにコミットされていない変更がないこと](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git)を確認しましょう)。
>>>>>>> main

```
git fetch origin
git checkout origin/trunk -B trunk
git checkout 30000-add-more-alots
git rebase trunk
git diff trunk 30000-add-more-alots > 30000.x.diff
<<<<<<< HEAD
```
=======
```
>>>>>>> main
