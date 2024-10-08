# ＣＳ立体図上で位置情報を共有するサイト（2024年能登半島地震災害支援に向けて）
## 本サイトを作成した理由
石川県立大学環境科学科流域環境学研究室では、2023年5月に珠洲地方で発生した地震が、山地の土砂災害に与えた影響について研究活動を行ってきました。
この研究の過程で現地の地形的特徴を把握するうえでCS立体図が大変役に立ちました。珠洲地方については、石川県によって2021年に航空レーザー測量が行われて、0.5mメッシュの詳細な地形データが整備されていました。
私たちは石川県からこの詳細地形データの提供を受けて、これを元に（国研）森林研究・整備機構森林総合研究所がCS立体図を作成し、これを研究に活用してきました。野外調査でGISを立ち上げるのは大変なので、WebGISとして多様な地理情報と重ね合わせて、地図上で位置情報を共有するサイトを作成しました。
当初は自分たちの研究用に作ったサイトですが、2024年1月1日の地震を受け、被災地の災害対策や復興に役立てていただきたいという思いから、このサイトを公開します。なにせ、完全なアマチュアが作ったものなので稚拙なところや改善点がたくさんあると思いますが、少しでも被災地の防災や復興に役立てていただければ幸いです。

## 使い方

### 地図を重ねて眺める
とりあえず、[GPSロケーション無しの最新バージョン](https://yokayoka.github.io/SuzuLocShare/index.html)を立ち上げてみてください。珠洲市中心部（飯田町付近）のCS立体図が表示されると思います。このCS立体図は2023年5月の地震以前のものです。ズームレベルは最大で17です。
右上にはレイヤーパネルのアイコンが表示されていると思います。このアイコンをクリックすると、CS立体図にオーバーレイ出来る地図群が表示されると思います。
現段階では、地理院地図（標準地図）、Googleによる高解像度画像、国土地理院によって2024年1月2日に撮影された空中写真の正射画像（輪島東地区、輪島中地区、珠洲地区）、国土地理院が判読した、斜面崩壊・堆積分布データ（国土地理院のgeojsonファイル）、国土地理院による1960年代撮影の正射写真、産業技術総合研究所による能登飯田の地質図、防災科学技術研究所による地すべり地形分布図を重ねることができます。地理院地図の標準地図のみ透過度を与えています。1月2日撮影の国土地理院の正射写真はズームレベルが14-18で表示されます。表示されないときはズームレベルを変えてみてください。
### 位置情報を共有する
CS立体図といろいろな地図を重ねて眺めていると、思わぬ発見があり、その場所を共有したくなる場合があります。このような位置情報の共有は防災上も大変重要です。画面左上にある二本の矢印が描かれた小さな四角いアイコンをクリックしてみてください。左側にパネルが現れると思います。共有したい場所を決めたら、まず場所の名前を地点名と書かれたテキストボックスに記入してください。その後、地図上でその場所をクリックすると、リンクのアドレスが表示されます。copyボタンを押すとそのアドレスが、クリップボードにコピーされますので、SNSやメールで位置情報を共有したい相手に送ってみてください。
受け取った相手が、リンクをクリックすると、本サイト上で同じ場所が現れるはずです。例えば、下記は狼煙漁港（高屋）の近くにある、岳山という場所です。これをブラウザーのURL欄にペーストすると岳山が表示されると思います。

https://yokayoka.github.io/SuzuLocShare/no_gps240110a.html?p=岳山&y=37.52069&x=137.23662
### CS立体図の地図タイルだけを使う
本サイトで利用している、能登地方びCS立体図の地図タイル（森林総研作成）をWMTS形式のデータとしてGISに読み込むには、下記のパスをGISに追加してください。
https://www2.ffpri.go.jp/soilmap/tile/cs_noto/{z}/{x}/{y}.png
WMTSタイルを読み込む方法については、それぞれのGISの解説を参照してください。プロジェクトの投影法がWebメルカトル (EPSG: 3857) になっていないと、表示されない可能性があるので、表示されない場合はプロジェクトの空間参照を確認してください。

## 謝辞
能登地域のCS立体図は、石川県森林管理課から提供を受けた航空レーザー測量のデータを元に森林総合研究所が[FME](https://fme.safe.com/solutions/data-types/gis-location-intelligence/)を利用して作成したものです。データを提供していただいた石川県森林管理課に感謝申し上げます。データの変換に際しては、Pacific Spatial Solutions 株式会社の飯島氏に大変お世話になりました。

能登地域のCS立体図は、石川県森林管理課より提供を受けた、航空レーザー測量のデータを元に作成したものです。データを提供していただいた石川県森林管理課に感謝申し上げます。

CS立体図は[ジオフォレスト社](https://gf17v.com/)の戸田堅一郎氏（元長野県）が発案した地形の可視化技術です。本サイトの作成においても多くのご助言をいただきました。ここに記して感謝します。
作成においてはgithubに公開された[Leaflet Copy Coordinates Control](https://github.com/zimmicz/Leaflet-Coordinates-Control)を改変して使用しています。作者に感謝いたします。

## 本サイトについて
### 免責事項
・本サービスの利用により生じた損害について、作者はいかなる責任も負わないものとします。

・本サービス及び本規約の内容は、予告なく変更、削除などがなされることがあります。

・本サイトに表示されるCS立体図は2021年以前のものです。2024年1月の地震により現地の地形は大きく変化していますのでご注意ください。

・位置情報に関しては、一定の誤差があります。とくに、2024年1月の地震により大きな地殻変動があった地域では、本サイトで表示される地形の位置情報が変化していることにご注意ください。

・本サービスでは複数の機関の地理情報データを使用しています。本サービスを介してこれらの地理情報データを利用する場合は、それぞれの機関の定める利用規約に従ってください。

# License
GNU General Public License v3.0

# Author
* 大丸裕武
    - 石川県立大学
* 村上　亘
    - 国立研究開発法人森林研究・整備機構森林総合研究所
