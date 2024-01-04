# ＣＳ立体図上で位置情報を共有するサイト（2024年能登半島地震災害支援に向けて）
## 本サイトを作成した理由
石川県立大学環境科学科流域環境学研究室では、2023年5月に珠洲地方で発生した地震が、山地の土砂災害に与えた影響について研究活動を行ってきました。
この研究の過程で現地の地形的特徴を把握するうえでCS立体図が大変役に立ちました。珠洲地方については、石川県によって2022年に航空レーザー測量が行われて、0.5mメッシュの詳細な地形データが整備されていました。
私たちは石川県からこの詳細地形データの提供を受けて、これを元に（国研）森林総合研究所に依頼してCS立体図を作成していただきました。野外調査でGISを立ち上げるのは大変なので、WebGISとして多様な地理情報と重ね合わせて、地図上で位置情報を共有するサイトを作成しました。
当初は自分たちの研究用に作ったサイトですが、2024年1月1日の地震を受け、被災地の災害対策や復興に役立てていただきたいという思いから、このサイトを公開します。
## 使い方
### 地図を重ねて眺める
とりあえず、[GPSロケーション無しの最新バージョン](https://yokayoka.github.io/SuzuLocShare/no_gps240104b.html)を立ち上げてみてください。珠洲市中心部（飯田町付近）のCS立体図が表示されると思います。このCS立体図は2023年5月の地震以前のものです。ズームレベルは最大で17です。
右上にはレイヤーパネルのアイコンが表示されていると思います。このアイコンをクリックすると、CS立体図にオーバーレイ出来る地図群が表示されると思います。
現段階では、地理院地図（標準地図）、Googleによる高解像度画像、国土地理院によって2024年1月2日に撮影された空中写真の正射画像（輪島東地区、輪島中地区、珠洲地区）、国土地理院が判読した、斜面崩壊・堆積分布データ（国土地理院のgeojsonファイル）、国土地理院による1960年代撮影の正射写真、産業技術総合研究所による能登飯田の地質図、防災科学技術研究所による地すべり地形分布図を重ねることができます。地理院地図の標準地図のみ透過度を与えています。1月2日撮影の国土地理院の正射写真はズームレベルが14-18で表示されます。表示されないときはズームレベルを変えてみてください。
### 位置情報を共有する


