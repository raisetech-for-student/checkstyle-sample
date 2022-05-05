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


# 導入方法

Checkstyle導入方法についてはmainブランチのコミットログを参考にしてください  
https://github.com/raisetech-for-student/checkstyle-sample/commits/main

CI失敗時にマージを禁止するサンプルは下記PRを参考にしてください  
https://github.com/raisetech-for-student/checkstyle-sample/pull/1

GitHubのレポジトリのSettings > BranchesからBranch protection ruleを追加します。
`Require status checks to pass before merging`にCheckstyleのワークフローを追加しましょう。
