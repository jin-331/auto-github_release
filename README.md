# GitHub Actions と semantic-release でリリースノートを自動作成する

### [semantic-release](https://github.com/semantic-release/semantic-release)とは

GitHub と連携するとタグとリリースノートを自動で作成してくれる。元々は、npm パッケージのバージョン管理や npm repository への publish を自動で行うためのツールらしい。  
private repo があがっちゃうことはない？？？

### commitlint & husky

semantic-release ではコミットメッセージが重要になる。
そのため、コミットメッセージに linter を導入する。

```
<type>(<scope>): <short summary>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope: animations|bazel|benchpress|common|compiler|compiler-cli|core|
  │                          elements|forms|http|language-service|localize|platform-browser|
  │                          platform-browser-dynamic|platform-server|router|service-worker|
  │                          upgrade|zone.js|packaging|changelog|docs-infra|migrations|ngcc|ve
  │
  └─⫸ Commit Type: build|ci|docs|feat|fix|perf|refactor|test
```

[引用](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type)
こんな感じで書く。  
上記の type によって自動でリリースノートにそのコミットがバグなのか軽微な修正なのかを判断して分けて記述してくれる。

[ref](https://dev.classmethod.jp/articles/github-actions-semantic-release-sample/)

[ref](https://zenn.dev/ucwork/articles/41cf2f20ecd2a0)
