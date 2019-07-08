# インストール

## 前提条件
macOS Mojave 10.14.5

## homebrewのインストール
homebrewとはパッケージマネージャーです。  
簡単に言うと色んなものをインストールするためのツールです。  
[ここ](https://qiita.com/_daisuke/items/d3b2477d15ed2611a058)などを参考にしhomebrewをインストールしてください。

## sbt
sbtとはビルドツールです。  
簡単に言うとScalaを実行するためのものです。  
以下よりsbtをインストールするための準備を行います。

### Javaのインストール
Javaとはプログラミング言語です。  
Scalaを動かすために必要なため、  
[こちら](https://www.java.com/ja/download/mac_download.jsp)からダウンロードし、インストールしてください。  
インストール後、`java -version`をターミナルで実行し、  
下記のようにバージョンが表示されればインストール成功です。

```bash
$ java -version
java version "1.8.0_111"
Java(TM) SE Runtime Environment (build 1.8.0_111-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.111-b14, mixed mode)
```

### sbtのインストール
sbtをインストールします。  
`brew install sbt`  
インストール完了後、  
`sbt about`を実行し、  動作することを確認します。  
初回起動はめちゃくちゃ遅いですが気長に待ってください。  
下記のように出ればインストール成功です。  
これにてScalaを実行する準備は出来ました。  
```bash
$ sbt about
[info] Updated file /Users/user/project/build.properties: set sbt.version to 1.2.8
[info] Loading settings for project global-plugins from idea.sbt ...
[info] Loading global plugins from /Users/user/.sbt/1.0/plugins
[info] Loading project definition from /Users/user/project
[info] Updating ProjectRef(uri("file:/Users/user/project/"), "user-build")...
[info] Done updating.
[info] Set current project to user (in build file:/Users/user/)
[info] This is sbt 1.2.8
[info] The current project is ProjectRef(uri("file:/Users/user/"), "user") 0.1.0-SNAPSHOT
[info] The current project is built against Scala 2.12.7
[info] Available Plugins
[info]  - sbt.ScriptedPlugin
[info]  - sbt.plugins.CorePlugin
[info]  - sbt.plugins.Giter8TemplatePlugin
[info]  - sbt.plugins.IvyPlugin
[info]  - sbt.plugins.JUnitXmlReportPlugin
[info]  - sbt.plugins.JvmPlugin
[info]  - sbt.plugins.SbtPlugin
[info] sbt, sbt plugins, and build definitions are using Scala 2.12.7
```
