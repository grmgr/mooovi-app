# mooovi

## 概要
Railsのカリキュラム学習にて作成しました。
自分が見た映画のレビューを投稿することができ、他の人のレビューも見ることができるアプリケーションです。
機能・学んだ点は下記の通りです。

- ユーザー登録、ログイン機能
- スクレイピングで作品情報表示
- 作品検索機能
- レビューの投稿
- コメント機能
- 評価（いいね）機能

## サンプル画像
[![Image from Gyazo](https://i.gyazo.com/dd0a567b9dd2d0ade37bdb9a07995c8e.gif)](https://gyazo.com/dd0a567b9dd2d0ade37bdb9a07995c8e)

# DB設計
//TODO:DB設計完成

## users
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|index: true|
### Association
- has_many :reviews

## reviews
|Column|Type|Options|
|------|----|-------|
|rate|||
|review|||
|prodct_id|||
|user_id|||
### Association
bilongs_to :user
bilongs_to :product

## products
|Column|Type|Options|
|------|----|-------|
|title|||
|image_url|||
|director|||
|detail|||
### Association
- has_many :reviews

## ar_internal_metadata
|Column|Type|Options|
|------|----|-------|
|key|||
|value|||

## active_storage_blobs
|Column|Type|Options|
|------|----|-------|
|key|||
|filename|||
|metadata|||

## active_storage_attachments
|Column|Type|Options|
|------|----|-------|
|name|||
|record_type|||
|record_id|||
|blob_id|||

## 感想
作成二つ目のrailsアプリケーション。
どんなアプリケーションでも必要になりそうなメソッドが多く、データの取得に使うメソッドは把握しておきたいと思う。
（完成：2019.08.)
