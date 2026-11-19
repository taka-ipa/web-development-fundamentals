# Day03 HTTP

1.HTTPとは何ですか？ また、HTTPリクエストとHTTPレスポンスの違いを説明してください。
・ブラウザなどのクライアントがサーバーと情報をやりとりする通信ルール
・リクエストはブラウザからサーバー側に要求
・レスポンスはサーバーからブラウザ側に返信

2.GET・POST・PUT・PATCH・DELETEの役割をそれぞれ説明してください。
GET　データ取得
POST　データ送信・作成
PUT　リソースの置き換え　丸ごと更新
PATCH　一部更新
DELETE　削除

GETは主にURLで「何が欲しいか」を指定し、POSTは主にBodyで「何を送るか」を指定する。
※厳密にはGETのBodyがHTTPの仕様上完全に禁止されているわけではないけど、一般的なWeb APIでは使わないと覚えて大丈夫！

3.HTTPリクエストのHeaderとBodyは、それぞれ何のために使われますか？ 具体例も挙げてください。
・ヘッダー　返すデータ形式の追加情報 Host Content-Typeとか 
・ボディ　サーバーへ送るデータ本体

4.HTTPレスポンスのStatus Code・Header・Bodyの役割をそれぞれ説明してください。
・Status Code　処理結果を数字で表す。201 は作成成功。
・Header　返すデータの形式などの追加情報。
・Body　クライアントへ返すデータ

5.Next.jsからLaravel APIを使って試合データをMySQLに保存するまでの流れを、HTTPリクエスト・SQL・HTTPレスポンスという言葉を使って説明してください。
・Next.jsがLaravelのAPIに POST /api/matches を送信
・Laravelがバリデーションなどを行い、MySQLにINSERT
・MySQLの保存結果をLaravelが受け取る
・LaravelがNext.jsにHTTPレスポンスを返す