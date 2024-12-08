# CustomNickName

カスタムフォントを使用し、プレイヤーの名前を変更するデータパック

> [!WARNING]
> 名前を変更する際、teamに加入させるので、元々入っていたteamからは強制的に脱退してしまいます。
> 
> ご理解の上、ご使用ください。



## 動作を確認しているバージョン

Minecraft Java Edition 1.21 ~

## 前提リソースパック

このデータパックは以下のリソースパックの導入を前提としています。

<b> [Negative Space Font](https://github.com/AmberWat/NegativeSpaceFont) </b>


## 使い方

  ### 基本
  1. [apply](#apply)
  2. [clear](#clear)
  
  ### 一般的には使用しないもの
  3. [cache](#cache)
  4. [init](#init)

<br>

  #### apply

  入力された文字を変更後の名前として、実行したプレイヤーに適応させます。
  
  エンティティを使用するため、読み込まれているチャンク内で実行してください。

  ```nim

  # 変更後の名前は fuga とする
  data modify storage custom_nick_name: input set value "fuga"

  # 名前を変更したいプレイヤーを実行者にして実行
  function #cnn:apply

  ```

<br>

  #### clear

  実行したプレイヤーのニックネームをリセットします

  ```nim

  # ニックネームをリセットしたいプレイヤーを実行者にして実行
  function #cnn:clear
  
  ```

<br>
<br>
<br>


  > [!CAUTION]
  > これから先のコマンドは、挙動がおかしくなった場合にのみ使用してください。
  > 
  > コマンド実行中に使用すると、処理が正しく行われない可能性があります

  
  #### cache

  一時保存したデータを削除します。

  ```nim

  function cnn:api/cache

  ```


  #### init

  データパックに必要なデータを初期化します

  ```nim

  function cnn:api/init
  
  ```


## 連絡先

<https://twitter.com/hikoma0000>

## ライセンス / LICENSE

These codes are released under the MIT License, see LICENSE.
  
