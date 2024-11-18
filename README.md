## アプリケーション管理システム

##　概要
このシステムでは、Webアプリとして登録されているアプリケーションの管理を行うことができます。また、管理者は登録ユーザーの管理も行うことができます。

アプリ情報の新規登録から編集、削除を行うことができ常に最新の情報を提示できます。ユーザー情報の場合も同様にできます。

## 主な機能
<全体>
- ログイン・ログアウト機能
- メニューバー(アプリ管理、ユーザー情報管理)

<アプリ管理>
- アプリ一覧画面
- アプリ一並べ替え、絞り込み機能
- アプリ新規登録、編集、削除機能（管理者のみ）
- アプリ検索機能->キーワード検索、価格範囲検索、ダウンロード範囲検索（管理者のみ）

<ユーザー管理>
- ユーザー情報一覧（管理者のみ）
- ユーザー情報新規登録、編集、削除機能（管理者のみ）
- ユーザー情報検索機能（管理者のみ）

## 開発環境
php 8.2.0
MySQL 5.7.39
Lalavel 10.13.5

## 設計書
[設計書ページへ](https://drive.google.com/drive/folders/1n0Iq23KKRWRBRwMB14UZI20sU9OYyglR?usp=drive_link)

## システム閲覧
[アプリケーションページへ](https://application-management-856b0a1acbaf.herokuapp.com)

## テストアカウント情報
```
<一般利用者>
メールアドレス：tech.taro@gmail.com
パスワード：tech0603

<管理者>
メールアドレス：tech.hyu@gmail.com
パスワード：tech0602
```


* Gitクローン
* .env.example をコピーして .env を作成
* MySQLのデータベース作成（名前：item_management）
* Macの場合 .env の DB_PASSWORD を root に修正（Windowsは修正不要）

    ```INI
    DB_PASSWORD=root
    ```

* APP_KEY生成

    ```console
    php artisan key:generate
    ```

* Composerインストール

    ```console
    composer install
    ```

* フロント環境構築

    ```console
    npm ci
    npm run build
    ```

* マイグレーション

    ```console
    php artisan migrate
    ```

* 起動

    ```console
    php artisan serve
    ```
