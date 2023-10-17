# テーブル設計

## users テーブル

| Column             | Type   | Options             |
| ------------------ | ------ | ------------------- |
| email              | string | null: false, UNIQUE |
| encrypted_password | string | null: false         |
| name               | string | null: false         |
| profile            | string | null: false         |
| occupation         | string | null: false         |
| position           | string | null: false         |


## prototypes テーブル

| Column     | Type      | Options                        |
| ---------- | --------- | ------------------------------ |
| title      | string    | null: false                    |
| catch_copy | text      | null: false                    |
| concept    | text      | null: false                    |
| user       | reference | null: false, foreign_key: true |



## comments テーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| content     | text       | null: false                    |
| prototype   | references | null: false, foreign_key: true |
| user        | references | null: false, foreign_key: true |