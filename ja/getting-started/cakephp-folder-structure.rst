CakePHP のフォルダ構造
######################

CakePHP をダウンロードして展開すると、次のようなファイルとフォルダが含まれているはずです:

-  app
-  lib
-  vendors
-  plugins
-  .htaccess
-  index.php
-  README

主要な三つのフォルダに注目してください:

-  *app* フォルダは、作成するプログラムが入る場所です。
   あなたのアプリケーションのファイルはここに入れます。
-  *lib* フォルダは、開発チームが作成したプログラムが入る場所です。
   このフォルダの中のファイルを勝手に編集 **しない** と誓ってください。
   これはコア (心臓部分) で、ここをいじってしまうと、私たちはもう助けを差し伸べることができません。
   代わりに :ref:`application-extensions` の修正方法を調べてください。
-  最後の *vendors* フォルダは、あなたが必要とする外部作成の PHP ライブラリを置いて、
   CakePHP アプリケーションで使用できるようにする場所です。

App フォルダ
============

アプリケーション開発の大部分は、CakePHP の *app* フォルダ内で行われます。
*app* の内部フォルダについて調べてみましょう。

Config
    CakePHP が使用する（数個の）設定ファイルが入る場所です。
    データベース接続の詳細、ブートストラップ、コアの設定ファイルなどがここに入ります。
Console
    アプリケーションのコンソールコマンドやコンソールタスクを含みます。このディレクトリは、
    bake の出力をカスタマイズするための ``Templates`` ディレクトリも含みます。
    詳しくは、 :doc:`/console-and-shells` をご覧ください。
Controller
    アプリケーションのコントローラとコンポーネントが入ります。
Lib
    サードパーティ、外部ベンダからのライブラリではなく、ファーストパーティのライブラリが入ります。
    これはベンダライブラリと内部ライブラリの構成を分割することを可能にします。
Locale
    国際化のための文字ファイルが入ります。
Model
    アプリケーションのモデル、ビヘイビア、データソースが入ります。
Plugin
    プラグインパッケージが入ります。
Test
    このディレクトリは、アプリケーションの全てのテストケースやフィクスチャを含みます。
    ``Test/Case`` ディレクトリは、あなたのアプリケーションを反映し、あなたのアプリケーションの
    クラスごとに１つかそれ以上のテストケースを含むべきです。
    テストケースやフィクスチャの詳細は、 :doc:`/development/testing` をご覧ください。
tmp
    CakePHP が一時的なデータを保管する場所です。保管される実際のデータは、CakePHP の
    設定しだいですが、このフォルダは通常、モデルの内容デ ータや、ログの保管に使用されます。
    時にはセッション情報も入ります。

    確実にこのフォルダが存在し、書き込み可能であるようにしてください。
    そうしないと、アプリケーションのパフォーマンスは激しく影響をうけることになります。
    デバッグモードでは、CakePHP がそうなっているかどうかを警告してくれます。

Vendor
    外部（サードパーティ）で作成されたクラスやライブラリは、ここに置いてください。
    そうすることで、App::import('vendor', 'name') で簡単にアクセス できるようになります。
    注意深く見ている人は、これは重複しているのではないか、と言うかもしれません。
    ディレクトリ構造のいちばん上にも *vendors* フォルダがあるからです。
    この二つのフォルダの違いは、複数のアプリケーションを動作させて、
    より複雑なシステムセットアップをする場合のことを考える際に取り扱います。
View
    表示用のファイルはここに置きます。エレメント、エラーページ、ヘルパー、レイアウト、
    ビューのファイルなどです。
webroot
    運用時 (*production*) 用のセットアップでは、このフォルダがアプリケーションの
    ドキュメントルートになります。CSS スタイルシートや画像、JavaScript ファイルを入れるための
    フォルダもあります。


.. meta::
    :title lang=ja: CakePHP Folder Structure
    :keywords lang=ja: internal libraries,core configuration,model descriptions,external vendors,connection details,folder structure,party libraries,personal commitment,database connection,internationalization,configuration files,folders,application development,readme,lib,configured,logs,config,third party,cakephp
