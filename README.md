# display-photos-for-stereogram
立体視のために空中写真を並べて表示するサイト

国土地理院が災害対応等により提供している垂直写真を２枚並べて表示し、立体視をするためのサイトです。立体視のための画像の拡大・縮小・回転などもある程度行えるようにしています。また写真測量などを考慮した特別な調整などは行っておらず、あくまで、「国土地理院が提供している写真を並べて、手動で調整することができる」という趣旨のサイトとなります。

読み込むデータについて、国土地理院が提供する geojson 単位となります。URL のクエリに `dataUrl={データの URL}` を指定することで、目的の geojson データを読み込むことが可能です。ただし、データの属性値などは直近（令和６年能登半島沖地震）のデータを参考に作成しており、そこから仕様が変更されるとエラー等が発生する場合があります。

国土地理院の空中写真の提供方法として、画像で提供される場合と、写真の拡大・縮小・スクロールが可能なサイトとして提供される場合があります。画像で提供される場合は、MapLibre GL JS を用いて、拡大・縮小・スクロールが可能となるようにし、サイトの場合は `<iframe>` で埋め込んでいます。

## 例
令和６年能登半島地震 空中写真リスト（1/12 現在）
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_suzu_0102suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_suzu_0105suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimahigashi_0102suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimanaka_0102suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimanaka_0105suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimanaka_0111suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimanishi_0105suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_wajimanishi_0111suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_anamizu_0105suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_anamizu_0111suichoku/2/3/1.geojson#8/37.277/136.941
* https://mghs15.github.io/display-photos-for-stereogram//?dataUrl=https://maps.gsi.go.jp/xyz/20240102noto_nanao_0105suichoku/2/3/1.geojson#8/37.277/136.941

## 参考
* 地理院地図 https://maps.gsi.go.jp/
* 国土地理院 令和6年(2024年)能登半島地震に関する情報 https://www.gsi.go.jp/BOUSAI/20240101_noto_earthquake.html

