# Rider-S

[![apm](https://img.shields.io/apm/l/vim-mode.svg)](https://github.com/0918nobita/Rider-S)

安全なサイクリングをサポートする AMP 対応 Web サービス

- スマホで Rider-S の Web ページを表示して、ホルダー等でハンドルに固定して使う。
- サイクリングを開始する前に、 Strava の My ルート作成機能等を使用して、移動経路をデータ化した GPX ファイルを用意してクラウドストレージに保存しておく。
- Rider-S で「位置情報取得」と「クラウドストレージ連携」の設定を有効にして、クラウドストレージ上の GPX ファイルを指定して読み込ませる。
- スマホの自動画面ロックの設定を解除して、時間経過で画面がロックされないようにしておく。
- Rider-S は「読み込んだ GPX ファイルの情報」と「位置情報」と「ジャイロセンサの情報」を組み合わせて解析し、メイン画面中央に大きな矢印を表示して運転者に進行方向を知らせる。
- メイン画面中央の矢印の下には、次に右折/左折するまでの移動距離が表示される。
- ArcGIS の API を利用して、移動経路付近の交通事故多発地点を取得し、その地点に近づくとアラートと画面の点滅によって運転者に注意を促す。
- UI は視界の悪い場所でもよく見える配色にする。
- サーバーサイドには Express を採用
- サーバー/クライアント間の通信には GraphQL を採用
- Service Worker を使用してバックグラウンドでも動作する (必要であれば音声案内もする)
- 音声には VOICEROID を使用する (申請が必要)
- Strava API v3 を使用して自転車の走行記録を取得し、目的地までのルートが自転車で走行可能かどうかの判断材料にする
