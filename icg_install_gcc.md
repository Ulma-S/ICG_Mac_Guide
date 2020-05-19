 ## iCG 環境構築 (Macユーザー向け)

---

### はじめに

MacのデフォルトのC++コンパイラはclangなので、今回の授業に対応するにはg++をインストールする必要があります。

```sh
gcc --version
g++ -v
```

このコマンドをそれぞれ実行して"Apple Clang…"という表示が出た場合は以下を実行してください。



---

### Homebrewのインストール

Homebrewはパッケージマネージャーです。パッケージマネージャーを使うことで追加アプリケーションを一括管理することができます。

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

ターミナルを開き、上のコマンドを実行してください。

途中パスワードが聞かれた場合はMacのログインパスワードを入力してください。



---

### gccのインストール

Homebrewを使ってgccをインストールします。

```sh
brew install gcc
```

このコマンドを実行してください。

しばらくするとインストールが完了します。

続いて今入れたgccをコマンドから呼び出せるようにパスを通します。

```sh
ls /usr/local/bin | grep gcc
ls /usr/local/bin | grep g++
```

上のコマンドをそれぞれ実行してください。

gcc-9などが一覧で表示されていると思います。

```sh
ln -s /usr/local/bin/gcc-9 /usr/local/bin/gcc
ln -s /usr/local/bin/g++-9 /usr/local/bin/g++
```

上のコマンドを実行してください。gcc-9, g++-9は各自のバージョンに合わせて変えてください。



```sh
sudo vi ~/.bash_profile
```

このコマンドを実行してください。vimエディタで編集します。

iを入力しINSERTモードに変更します。

```sh
export PATH=$PATH:/usr/local/bin
```

この一文を適当な場所に貼り付けてください。

終わったらescキーを押してINSERTモードを終了し、:wqと入力してvimエディタを閉じてください。

ここまでできたらターミナルを再起動してください。

---

これで一通り終了です。お疲れ様でした！



参考：https://qiita.com/wawawa/items/50c2c612b0937f28d92b