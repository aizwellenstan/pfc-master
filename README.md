# 概要
カロリーとPFC（タンパク質, 脂質, 炭水化物）を記録し体重をコントロールするためのダイエットアプリです。   
毎日の食事やカロリーをグラフやカレンダーで可視化することで、ダイエットを続けるモチベーションを維持しやすくなります。  

#### URL
この項目はあとで追記する。
#### テストアカウント
最初の画面の「ログイン」をクリック→ログインページに遷移→「かんたんログイン」をクリック  
上記の流れでゲストユーザーとしてログイン可能となっております。

# 機能一覧
- ユーザー新規登録, 編集機能    
- ログイン・ログアウト機能  
- 食事記録（食べたもの, カロリー, PFC値, 体重, 写真）の投稿, 編集, 削除機能 
- コメント機能(Ajaxで非同期化)
- いいね機能(Ajaxで非同期化)
- 自動計算機能（体重を入力すると最適なカロリー目標値, PFC値目標値が自動計算されます）
- グラフ機能（1日毎の合計カロリーと1日毎の体重が確認できます）
- フォロー機能  
- ページネーション機能
- カレンダー機能（カレンダーで1日毎の食べたもの, カロリー,体重を確認できます）
- 食事履歴の確認機能（マイページからその人の今までの食べたもの, カロリー, PFCの一覧を確認できます）

# 使用言語・使用技術一覧
#### フロントサイド
- Haml  
- Scss  
- jQuery  
- boostrap4  

#### バックエンド
- Ruby 2.5.1  
- Rails 5.2.4.3 

#### ユーザー関連
- devise

#### 画像関連
- carrierwave

#### グラフ関連
- chart.js

#### サーバー
- Nginx

#### データベース
- MySQL 5.6.47  

#### インフラ・開発環境
- AWS（VPC, EC2）
- Capistrano
- RSpec  

# AWS構成図
この項目はあとで追記します。

# ER図  
この項目はあとで追記します。

# 制作背景
私自身が「ダイエットが続かない」という悩みを抱えていたため、自分と同じような「ダイエットが続かず困っている人」をユーザーと想定し、**"ダイエットを続けやすくする"** という目的で制作しました。  
ダイエットが続けられない理由を以下のように分析しました。

- 何をどれくらい食べれば体重が減るのかわからない
- 目標に近づいているのかどうかわからない

これらの点を解決するために下記の工夫を行いました。

# 工夫した点

#### 目標の自動設定（自動計算）
体重を入力すると、自動で1日のカロリー目標, PFC目標が設定されるようにしました。
1日のどれくらい食べればいいのかがわかることで、食事管理しやすくなると考えました。

#### プロセスの可視化
グラフ, カレンダー, Instagramのような画像一覧ページを実装し、ダイエットの進捗を目に見える形で確認できるようにしました。  
目標に近づいているかどうか確認できたり、日々の頑張りが目に見えて確認できたりすることで継続するモチベーションが維持しやすくなると考えました。  
