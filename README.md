# mytweet
## 機能一覧

------

### User機能

- Userがログイン/ログアウト/サインアップできる
- ログインしているUserのヘッダーにはUserの名前と投稿ボタンを設置
- ログインしていないUserのヘッダーにはサインイン・サインアップボタンを設置
- 自分のツイートを一覧表示できる(マイページ)

### ツイート機能

- Userがツイートを投稿できる
- Userが自分のツイートを編集できる
- Userが自分のツイートを削除できる
- Userはツイートの詳細（コメント）を閲覧できる
- ログインしていなくても全てのブログを閲覧できる

### コメント機能

- Userがツイートに対してコメント投稿できる。



## テーブル設計

------

* Usersテーブル

| カラム論理名 | カラム物理名       |
| ------------ | ------------------ |
| ID           | id                 |
| ユーザ名     | username           |
| パスワード   | encrypted_password |



* Tweetsテーブル

| カラム論理名 | カラム物理 |
| :----------- | :--------- |
| ID           | id         |
| ユーザID     | user_id    |
| 本文         | text       |



* Commentsテーブル

| カラム物理名 | カラム論理名 |
| ------------ | ------------ |
| ID           | id           |
| ユーザID     | user_id      |
| TweetsID     | tweet_id     |
| 本文         | text         |

