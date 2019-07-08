# プロジェクトの読み込み
作成したプロジェクトをIntellij IDEAで読み込みます。  
IntelliJ IDEAを開き、importをクリックしてください。  
![top](/img/setup/import-project/top.jpg)  
  
クリックすると、フォルダを選択させられるので、  
前ページで作成したtutorialフォルダを選択し、openをクリックしましょう。  
![select-folder](/img/setup/import-project/select-folder.png)  

openをクリックすると以下のようなものが表示されるので、  
**import project from external model**にチェックをし、  
**sbt**を選択して、**Next**をクリックしてください。  
![import-project](/img/setup/import-project/select-build-tool.png)  

以下のような画面が表示されます。  
チェックボックス等色々ありますが、**なにもいじらず**そのまま**Finish**を押しましょう。    

Project JDKの項目が選択されていない場合、  
Javaのインストールに失敗しているので、[インストール](install.md)のJavaの項目をやり直すか、  
調べて各自解決方法を模索してみてください。  
![settings](/img/setup/import-project/settings.png)  

**Finish**を押すと、Projectが開かれます。  
そのとき、右下にScalaプロジェクトを読み込こんでいる表示がされますので、  
表示がなくなるまで待機しましょう。  
(processes running...という文字、またはプログレスバー)
![importing](/img/setup/import-project/importing.png)  


表示がなくなれば、読み込んだプロジェクトを確認しましょう。  
左上にある**Project**というタブをクリックすると、読み込んだプロジェクトが表示されます。  
このとき、`.idea`というフォルダが作成されていることが確認できます。  
これはIntelliJ IDEAがフォルダを開いたときに作成されるものです。  
気にしないでください。  
![file-tree](/img/setup/import-project/file-tree.png)


前回作成した`HelloWorld.scala`をIntelliJ IDEAで実行してみましょう。  
メニューバーの**Run**内にある、**Run Hello World**をクリックすると実行されます。  
結果は下部に表示されます。  
![run](/img/setup/import-project/run.png)


このページでの最終的なフォルダ構成は以下になっています
```
tutorial/
┣ .idea/
┣ project/
┣ target/
┣ HelloWorld.scala
┗ build.sbt
```
