# laravel8-docker-template

* 開発開始時
```
1. $ docker-compose up --build -d
2. $ docker-compose exec app bash
3. .envの作成(.env exampleを複製しファイル名を.envに変更)
4. $ php artisan key:generate
```

* 開発時
```
server: http://localhost:8000/
phpmyadmin: http://localhost:8080/
```

* gitにpush
```
1. git add .
2. git commit -m "<コメント>"
[update]・・・機能修正(バグ関係ではない)
[add]・・・新規ファイル追加
[fix]・・・バグ修正
[remove]・・・削除(ファイル)
例：$git commit -m "[update] カレンダー機能の追加" $git commit -m "[add] 開発環境の構築"

3. git push origin <リポジトリ名>
```

* 開発終了時
```
1. $ exit
2. $ docker-compose down
```

* その他時やること
```
venderフォルダがないとき
$ composer update

APP_KEYが設定されてないとき
$ php artisan key:generate

.envが反映されないとき
$ php artisan cache:clear
$ php artisan config:cache

データベースのテーブルの中身をリセットしたいとき
$ php artisan migrate:fresh
```