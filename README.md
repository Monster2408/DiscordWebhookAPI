<h1 align="center">JoinChecker</h1>



##### README記述法について
- 非推奨については~~伏字~~という形で表記
##### 鯖参加時のチェックシステム
- Discord参加者限定のみ
##### チャットシステム
- コンフィグよりチャットチャンネルやコンソールチャンネルなどを設定可能
- コンソールチャンネルにログを表示
- コンソールチャンネルにてコマンド実行可能
##### 追加予定
- スポンサー限定
  - Ko-fiにてスポンサー限定Discordシステム完成済み
  - Ko-fiページ https://ko-fi.com/mlserver
  - Tierごとに別々の役職が付与されるためプレイヤーの連携済み役職を取得したら問題なし
  
<h1 align="center">ChannelSubChecker</h1>

### YouTube登録者限定機能
#### 申請方法
- ChannelSubCheckerの<a href="https://sub-join.mlserver.xyz" target="_blank">特設ページ</a>から順に可能。
#### 設定
- `/jc y`でモードの切り替え
- JoinCheckerのコンフィグファイルで`JoinChecker.YouTube`をTrueで初期値をONにできる。

```yml
JoinChecker:
    YouTube: True
    Normal: False
    Admin: False
```

#### 参加者(現在は運営含む)
- 企画参加直前に申請する(目安10時間前まで)
  - 企画時間を2時間と計算した場合

#### 仕様
- 申請せずに参加すると<a href="#3">「申請していない」</a>通りである。
- 申請から12時間経過して参加しようとすると<a href="#2">「期限切れ」</a>通りである。
- <a href="#1">「APIに問題があった」</a>通りである。

#### 参加時
<h5 id="3">申請していない</h5>
一度も申請したことがない人は「まだ一度も参加申請されていません。」と言われて参加できない。
https://i.gyazo.com/c109c3d6e2ac7afe223c546b1171be78.png

<h5 id="2">期限切れ</h5>
申請から12時間経過している。メッセージは「アクセストークンの有効期限が切れています。もう一度申請しなおしてください。」と表示される。
https://i.gyazo.com/df81f28f3c84627e173838509c6617b1.png

<h5 id="0">APIに問題があった</h5>
これは普通に企画開催の問題がある^👅^。メッセージは「APIでエラーが発生しました。」と表示される。
https://i.gyazo.com/d4b078418150d869d250e5ff10d302c2.png

<h5 id="1">チャンネル登録していない</h5>
申請時には登録必須だが12時間以内なら解除しても参加可能。