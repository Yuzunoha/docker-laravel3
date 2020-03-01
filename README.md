# docker-laravel3

## 意気込み
- 10回でも20回でも試す。覚えるまで試す
  - がんばろう

## 参考
- [Dockerを使ってLaravel開発環境構築][link1]

## メモ
### cloneしたPCで必要な作業 
- アクセス許可
  ```
  # phpコンテナで
  chmod 777 -R *
  ```
- .envをコピーしてキー生成
  ```
  # phpコンテナで
  php artisan key:generate
  ```
- DB_HOSTはコンテナ名でいける
  ```
  DB_CONNECTION=mysql
  DB_HOST=db-host
  DB_PORT=3306
  DB_DATABASE=database
  DB_USERNAME=docker
  DB_PASSWORD=docker
  ```
- migrationファイルで管理するから`docker/db/data`あたりは除外

[link1]:https://qiita.com/A-Kira/items/1c55ef689c0f91420e81