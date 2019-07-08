# プロジェクトの作成
Scalaのプロジェクトを作成するのは簡単です。  
というのもbuild.sbtというファイルを用意するだけで良いのです。  
早速Scalaプロジェクトを作成していきましょう。

まず、好きなディレクトリにフォルダを作成します。  
今回はtutorialという名前にします。
```bash
$ mkdir tutorial
```

tutorialフォルダに移動し、
**build.sbt**というファイルを作成します。  

```bash
$ cd tutorial
$ echo 'sbt.Version := "1.2.8"' >> build.sbt
$ echo 'scalaVersion := "2.12.8"' >> build.sbt
```

build.sbtにはsbt.Versionと、scalaVersionというものを設定しました。  
これは名前の通り、使用するsbtのversionとScalaのVersionを指定するものです。
理由がない限り最新のものを指定するようにしましょう。


### Scalaファイルの作成
tutorialフォルダの中にScalaファイルを作成します。  
ここでは**HelloWorld.scala**というファイル名にします。  
```bash
$ touch HelloWorld.scala
$ cat <<EOL >> HelloWorld.scala
object HelloWorld {
  def main(args: Array[String]): Unit = {
    println("Hello, World!")
  }
}
EOL
```

HelloWorld.scalaには、文字を表示するだけのするだけのコードを書き込みました。  
説明は追々行うので今は何も考えなくて良いです。  
現在のフォルダの構成は以下の通りです。  

```
tutorial/
┣ HelloWorld.scala
┗ build.sbt
```

### Scalaの実行
sbtというコマンドを打つことで、sbtを起動します。   
起動時に`target`と`project`というフォルダが作成されますが気にしないでください。
```sbt
$ sbt
[info] Updated file /Users/user/workspace/scala/tutorial/project/build.properties: set sbt.version to 1.2.8
[info] Loading settings for project global-plugins from idea.sbt ...
[info] Loading global plugins from /Users/user/.sbt/1.0/plugins
[info] Loading project definition from /Users/user/workspace/scala/tutorial/project
[info] Updating ProjectRef(uri("file:/Users/user/workspace/scala/tutorial/project/"), "tutorial-build")...
[info] Done updating.
[info] Loading settings for project tutorial from build.sbt ...
[info] Set current project to tutorial (in build file:/Users/user/workspace/scala/tutorial/)
[info] sbt server started at local:///Users/user/.sbt/1.0/server/0fe1cafaf854ea3f542d/sock
sbt:tutorial>
```

起動に成功すると、`sbt:tutorial>`と表示されます。  
tutorialの部分は作成したフォルダ名が表示されているので、別名で作成した場合はそれに応じた名前が表示されています。  
それでは先程作成したコードを実行します。  
```sbt
sbt:tutorial> run
[info] Updating ...
[info] Done updating.
[info] Compiling 1 Scala source to /Users/agoetc/workspace/scala/tutorial/target/scala-2.12/classes ...
[info] Done compiling.
[info] Packaging /Users/agoetc/workspace/scala/tutorial/target/scala-2.12/tutorial_2.12-0.1.0-SNAPSHOT.jar ...
[info] Done packaging.
[info] Running HelloWorld
Hello, World!
[success] Total time: 6 s, completed 2019/06/04 14:00:14
sbt:tutorial> 
```
runというコマンドで実行することが出来ます。
Hello, World!と表示されていることが確認できれば実行完了です。  
おめでとうございます。  
sbtを終了して終えましょう。  
exitと打ち込むことによってsbtを終了することが出来ます。
```
sbt:tutorial> exit
[info] shutting down server
```


このページでの最終的なフォルダ構成は以下になっています
```
tutorial/
┣ project/
┣ target/
┣ HelloWorld.scala
┗ build.sbt
```
