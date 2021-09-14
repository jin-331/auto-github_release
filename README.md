# GitHub Actions と semantic-release でリリースノートを自動作成する

[semantic-release](https://github.com/semantic-release/semantic-release)とは
GitHub と連携するとタグとリリースノートを自動で作成してくれる。元々は、npm パッケージのバージョン管理や npm repository への publish を自動で行うためのツールらしい。  
private repo があがっちゃうことはない？？？

[ref](https://dev.classmethod.jp/articles/github-actions-semantic-release-sample/)

## 上記のサイトだとうまくいかなかった

commitLint のところがうまく動かなかった。。。。

commit 単位ではなく PR 単位の方が管理しやすいのでは？

workflow を修正すればいける？？
PR のタイトルと本文からリリースノートを構成したい。

## commit で管理する方法

[ref](https://zenn.dev/ucwork/articles/41cf2f20ecd2a0)
