## Macユーザーガイド

---

- linuxコマンドリスト

  ```sh
  # ディレクトリの中身を見る
  ls
  
  # ディレクトリに移動する
  cd 
  
  # hogeを実行
  ./hoge
  ```

---

- デスクトップにDevelopディレクトリを作る

- ターミナルを開く

  

- Developに移動

  ```sh
  cd ~/Desktop/Develop
  ```

  - テキストエディタを開く

    - フォーマット/標準テキストにする
    - そのままだとリッチテキストになっているので、標準テキストにする必要があります

    

  - 適当に"Hello, World"を出力するプログラムを作成

    ```c++
    //helloworld.cpp
    #include <stdio.h>
    int main(){
      printf("Hello, world!\n");
      return 0;
    }
    ```

  - さっき作ったDevelop/に保存

  

- ターミナルに戻る

  ``` shell
  cd ~/Desktop/Develop
  ls
  # helloworld.cppが出てると思います
  ```

  

- 実行ファイル作成 

  ```sh
  # helloworld.cppをg++でコンパイルしたのち,
  # helloworldという実行ファイルを作る
  g++ helloworld.cpp -o helloworld
  ```

  

- 実行

  ```sh
  ./helloworld
  ```

---

- 知ってると便利

  ターミナルで同じコマンドを打つときは矢印の上下で前打ったコマンドを入力することができます

---

### 暇な人むけ

- 全部コマンドでHello, world

```sh
# プロジェクトフォルダとしてsampleを作る
cd ~/desktop/Develop
mkdir sample
cd sample

# main.cppを作る
touch main.cpp

# vimエディタで編集
vi main.cpp

# 開いたら"i"を押してINSERTモードにする
# 上と同じC++プログラムを入力する
# escapeキーを押して編集モードを終了
# ":wq"を入力して保存してエディタを終了

# コンパイルして実行ファイルを作成
g++ -o sample sample.cpp
# sampleができる

#sampleを実行
./sample

```

