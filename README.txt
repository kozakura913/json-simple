Please visit:
http://code.google.com/p/json-simple/

Github Packagesを使用せずGithubPagesを使用している理由
現在のGitHubでは認証機能を使用せず公開リポジトリをMaven依存関係に追加する事ができません
詳細は以下を参照
https://github.community/t/download-from-github-package-registry-without-authentication/14407

このリポジトリでは独自に以下の変更を施しています

互換性をJava8に変更します
JSONObjectがキーとして文字列のみを受け入れます
総称型(raw型)を使用しません
JUnit4.13.2を使用します

依存関係に以下を追加して利用します

<repositories>
	<repository>
		<id>io.github.kozakura913.json-simple</id>
		<url>https://kozakura913.github.io/json-simple/</url>
	</repository>
</repositories>
<dependencies>
	<dependency>
	<groupId>xyz.kzkr</groupId>
	<artifactId>json-simple</artifactId>
	<version>2.0.0</version>
	</dependency>
</dependencies>
