# アプリケーション名

groupOffice
=======

<img width="1160" alt="README" src="https://user-images.githubusercontent.com/75027499/107139750-e7b35a80-6960-11eb-95e4-d99fd7d00b75.png">

# 概要

グループウェアを作成しました

# アプリURL

- ゲストユーザーとしてワンタッチログインが可能です</br>
https://arti-cle.herokuapp.com/

# 目指した課題解決
- 企業内でのコミュニケーションを円滑に進めたい
- 同僚・上司などの予定を閲覧したい
- 納期管理の見える化

# DEMO
<!-- ## トップページ画面
<img width="1160" alt="top-image" src="https://user-images.githubusercontent.com/75027499/107139750-e7b35a80-6960-11eb-95e4-d99fd7d00b75.png">

## 新規登録画面
<img width="1159" alt="signup-image" src="https://user-images.githubusercontent.com/75027499/107141021-775d0700-6969-11eb-9d45-ef432f87b534.png">

## ログイン画面
<img width="1150" alt="login-image" src="https://user-images.githubusercontent.com/75027499/107141056-ae331d00-6969-11eb-92eb-a1e4632ac8b5.png">

## アーティスト一覧画面
<img width="1150" alt="artist-image" src="https://user-images.githubusercontent.com/75027499/108620206-e65c5480-746d-11eb-8eeb-cbbd764bde77.gif"> -->

# 使用技術(開発環境)
## フレームワーク
- laravel(6.20.19)
## CSSフレームワーク
- Bootstrap
## バックエンド
- PHP(7.3)
## フロントエンド
- HTML
- SCSS
- Javascript
- jquery
- ajax
## データベース
- MySQL
## テスト
- RSpec
## バージョン管理
- GitHub
## デプロイ環境
- heroku

<!-- # 追加実装予定項目
- カレンダー機能(マイページに表示予定)
- ユーザーフォロー機能
- DM機能(相互フォロー時のみ)
- アーティスト詳細項目(アーティスト公式ページへのリンクなど表示)
- メンション機能 -->

# ER図

<img width="577" alt="ER図" src="https://user-images.githubusercontent.com/75027499/107758434-3484a000-6d6a-11eb-8592-2872330be2cb.png">

# テーブル設計

## users テーブル

| Column             | Type    | Options                   |
|--------------------|---------|---------------------------|
| nickname           | string  | null: false               |
| email              | string  | null: false, unique: true |
| encrypted_password | string  | null: false               |
| department_name_id | integer | null: false               |
| affiliation_id     | integer | null: false               |

### Association

- has_many :plans

## newsletteres テーブル

| Column        | Type       | Options                        |
|---------------|------------|--------------------------------|
| title         | string     |                                |
| content       | text       | null: false                    |
| importance_id | integer    | null: false                    |
| user          | references | null: false, foreign_key: true |

### Association

- belongs_to :user

## address_books テーブル

| Column       | Type   | Options                   |
|--------------|--------|---------------------------|
| name         | string | null: false               |
| email        | string | null: false, unique: true |
| company_name | string | null: false               |
| position     | string | null: false               |

<!-- ### Association

- belongs_to :room
- belongs_to :user -->

## plans テーブル

| Column       | Type   | Options     |
|--------------|--------|-------------|
| plan_title   | string | null: false |
| plan_details | text   | null: false |

### Association

- be_longs :user
- has_many :messages

## Author
- https://github.com/Fuka-Aki
