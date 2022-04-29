# user テーブル

| column              | Type      | options                   |
| ------------------- | --------- | --------------------------|
| name                | string    | null: false               |
| email               | string    | null: false, unique: true |
| encrypted_password  | string    | null: false               |
| profile             | text      | null: false               |
| occupation          | text      | null: false               |
| position            | text      | null: false               |



# prototypes テーブル

| column      | Type        | options                         |
| ----------- | ----------- | ------------------------------- |
| title       | string      | null: false                     |
| catch_copy  | text        | null: false                     |
| concept     | text        | null: false                     |
| user        | references  | null: false, foreign_key: true  |



# commentsテーブル

| column      | Type        | options                         |
| ----------- | ----------- | ------------------------------- |
| content     | text        | null: false                     |
| prototype   | references  | null: false, foreign_key: true  |
| user        | references  | null: false, foreign_key: true  |
