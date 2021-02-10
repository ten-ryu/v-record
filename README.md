# README

# テーブル設計

## users テーブル

| Column          | Type   | Options     |
| --------------- | ------ | ----------- |
| username        | string | null: false |
| email           | string | null: false |
| password        | string | null: false |

### Association

- has_many :posts

## posts テーブル

| Column       | Type    | Options                        |
| -------------| ------- | ------------------------------ |
| user_id      | integer | null: false, foreign_key: true |
| time         | integer | null: false                    |
| memo         | string  |                                |

### Association

- belongs_to :user