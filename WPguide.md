
WPサイト更新説明書

---

# 更新手順

1. Wordpressにログインする
   - https://●●●●●.jp/wp-admin
   - 登録したユーザー名とパスワードでログインする
2. ダッシュボード　＞　投稿　＞　新規追加
   - タイトル、本文、アイキャッチ等を追加してOKなら右カラム「公開」から投稿する。
   - まだ公開しないのであれば右カラム「下書き保存」
   - 公開日設定や非公開設定も同じ右カラムの「公開」から可能

![WP画像1](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/01.jpg)


---

# 設定系

## タイトル
- 52文字まで
- 27文字以上はTOPで「...」で省略される


## アイキャッチ画像
右カラムの「アイキャッチ画像」で記事のサムネイルとメイン画像を追加（共通）
- サイズは 1100px × 430px

## カテゴリ
右カラムの「カテゴリー」でチェックする
追加するときは「＋新規カテゴリーを追加」か、投稿＞カテゴリーから追加する
- 長すぎる文字数はNG（だいたい10文字ぐらいまではOK）
- 最大2つまで（できれば1つが望ましい）
- カテゴリを選択しなかった場合、「その他」に自動振り分けされる

## スラッグ
記事に振り分けられるURLを指定できる
- 入力しなくても記事タイトルが自動で設定される（日本語だとURLが長くなる）
- カテゴリや他ページとの重複（干渉）を避けるために、日付をいれたりわかりやすいものにする

## 作成者
記事の作成者を選択。ユーザーから選ぶ
該当ユーザーからログインしてる場合は設定の必要がないと思われ

---


# 本文系

## 本文(段落)
**ビジュアルエディタ** ： 通常入力  
**テキストエディタ** ： ＜p＞タグを利用

## 大見出し
![h2](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/h2.png)  
**ビジュアルエディタ** ： 文をドラッグで選択し、「段落 ＞ 見出し2」を選択  
**テキストエディタ** ： ＜h2＞タグを利用

## 小見出し
![h3](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/h3.png)  
**ビジュアルエディタ** ： 文をドラッグで選択し、「段落 ＞ 見出し3」を選択  
**テキストエディタ** ： ＜h3＞タグを利用

## テキストリンク
![a](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/a.png)  
**ビジュアルエディタ** ： 文をドラッグで選択し、エディタ上部にあるチェーンアイコンの【リンクの挿入（⌘+K)】を選択。外部サイトへのリンクの際などには、設定アイコンから詳細画面を開き「リンクを新しいタブで開く」にチェックをつける  
**テキストエディタ** ： ＜a＞タグを利用

## 画像の追加（リンクなし）
**ビジュアルエディタ** ： 「メディアを追加」で画像を追加。「ファイルをアップロード」で画像をUPし、「メディアライブラリ」で追加する画像をした後、右下の「添付ファイルの表示設定」で「リンク先 ＞ なし」「サイズ ＞ フルサイズ」に設定する。適時「代替テキスト（alt）」も設定する  
**テキストエディタ** ： ＜img＞タグを利用。witdhとheightとaltは適時設定
- 表示領域の最大幅を超えた場合CSSで自動で縮小します

## 画像の追加（リンクあり）
**ビジュアルエディタ** ： ↑と同じように画像を追加し、「リンク先」で「カスタムURL」を選択しURLを入力  
**テキストエディタ** ： ``` <a href="" target="_blank"><img src="" width="" height="" alt=""></a>```

## 引用文
![bq](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/bq.png)  
**ビジュアルエディタ** : 文をドラッグで選択し、「”」アイコンを選択。スタイルが変われば適用されていることになる  
**テキストエディタ** ： ```<blockquote>この中に引用テキスト</blockquote>```
- テキストや画像を引用を引用した際は、引用元を記載する。

## ソースコードの挿入
![code](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/code.png)  
**ビジュアルエディタ** : 文（ソース）をドラッグで選択し、「コードブロック」から該当の言語を選択する。スタイルが変われば適用されていることになる  
**テキストエディタ** : 現状preとcodeでのスタイルを用意していません


## 色付き背景
![color1](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/color1.png)  
![color2](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/color2.png)  
![color3](https://github.com/bptakahashi/BP_wordpressguide/blob/master/img/color3.png)  
**ビジュアルエディタ** : 文をドラッグで選択し、エディタ上部にある【スタイル ▼】から選択する
  - bg_gray：グレーの背景
  - bg_yellow：黄色の背景
  - bg_green：緑色の背景

**テキストエディタ** : 何かかしらのタグで囲んで、classをあててください。


---

# 補足

### ヘッダーメニューについて
- 自動追加ではないため、カテゴリを追加するには手動で選んで追加する必要がある
- 追加するには、「外観 ＞ メニュー ＞ headerNav」の中身を「メニューの項目を追加 ＞ カテゴリー」から選ぶ
- 並びは、上から順番に左並びになる
- SPの場合は、ハンバーガーメニューで全カテゴリが表示される

### Recommend Post
- 記事のPV数を認識してそのTOP3が表示される

### Categoryカラム
- 存在しているカテゴリが全て表示される予定
- 最初から入っており削除できない「未分類」は表示されない
