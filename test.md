初めて作成されたリポジトリです。
-------------------------------

GitHub上でのリポジトリ作成からファイルのpushまで。

- リポジトリ作成
    - GitHubにログイン
    - Create Repository

- ローカルPCにリモートリポジトリをクローン
    - 作成したリモートリポジトリのURLをコピー
    - git clone <リモートリポジトリのURL>

- ローカルリポジトリで作成したファイルをgitHubに反映
    - git add <作成したファイル> ⇒ ステージングエリアにファイルを追加
    - git status ⇒ 現在ステージングエリアに存在するファイルを確認
    - git reset HEAD [ファイルパス] ⇒ ステージングを解除
    - git commit -m "コメント" ⇒ コメント付きでリポジトリにコミット
    - git push origin main ⇒ gitHubに反映
        - origin:clone元のリモートリポジトリ
        - main:ブランチ(mainはリモートリポジトリ作成時に作られたもの)

# おまけ
## ローカルリポジトリからリモートリポジトリへcommitするための設定

- ユーザ名を設定する
    git config --global user.name "ユーザ名"
- メールアドレスを設定する
    git config --global user.email "メールアドレス"

- 設定内容を確認する
    git config --global --list



## パスワードを毎回聞かれないために

- ヘルパーを設定する 
git config --global credential.helper wincred
 
- 設定内容を確認する
git config --global --list

- 初回だけログインがいる
Authorize GitCredentialManager
