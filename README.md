# このプロジェクトについて

CheckstyleをCIに導入するサンプルのプロジェクトです。

# 前提
- Java 17

# 利用しているCheckstyle

GoogleのCheckstyleを利用しています。  
https://github.com/checkstyle/checkstyle/blob/master/src/main/resources/google_checks.xml

# 実行方法
`./gradlew checkstyleMain`

実行すると`/build/reports/checkstyle`にレポートが出力されます。  

<img width="500" alt="checkstyle-1" src="https://user-images.githubusercontent.com/62045457/166938329-dd4e07a4-9fae-4ba3-afb3-27ad4a3066a1.png">

# 導入方法

Checkstyle導入方法についてはmainブランチのコミットログを参考にしてください  
https://github.com/raisetech-for-student/checkstyle-sample/commits/main

CIの設定ファイルは[checkstyle.yml](./github/workflows/checkstyle.yml)を参照してください。  
CI失敗時にマージを禁止するサンプルは[こちらのPR](https://github.com/raisetech-for-student/checkstyle-sample/pull/1)を参考にしてください。  
GitHubのレポジトリのSettings > BranchesからBranch protection ruleを追加します。  
`Require status checks to pass before merging`にCheckstyleのワークフローを追加しましょう。
