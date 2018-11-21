# MiniAxe組立説明書

## 天キーでお買い上げいただいた方へ
ボトムプレート用のねじが短くプレートが留められないというケースがありましたので、不具合の有無に関わらず、代替部品（ねじ、スペーサ）をお送りしています。つきましては、送付先をTwitter(@ka2hiro), Discord(@ka2hiro), Email(info@kagizaraya.jp)のいずれかまでお知らせください。

ご迷惑ならびにお手数をおかけしますが、よろしくお願いいたします。(2018/11/10)

## 組み立ての前に
* はんだごてや工具、部品等でのケガに注意してください。
* 作業中に席を離れるときは、はんだごての電源を確認してください。
* 非常に小さい部品が含まれていますので、失くさないように注意してください。

## 内容物の確認
キットには以下の部品が含まれています。作業前に不足がないか確認してください。

![キットの内容物](images/IMG_2761.jpg)

番号 | 名前      | 値     | 個数 | 備考                | 部品番号
:----|:--------|:-----|:----|:-----------------|:-------
1  | PCB      |       | 2    | 左右1枚ずつ         |
2  | 抵抗      | 10kΩ  | 5    | 予備1、緑シールまたはマーカ<sup>[1](#marker)</sup>、部品本体に"103"という表記あり | R1, R4
3  | 抵抗      | 22Ω   | 5    | 予備1、黄シールまたはマーカ<sup>[1](#marker)</sup>、部品本体に"220"という表記あり | R2, R3
4  | コンデンサ | 1μF | 5   | 予備1、青シールまたはマーカ<sup>[1](#marker)</sup>、色が濃い | C1, C3
5  | コンデンサ | 0.1μF | 3 | 予備1、シールなし    | C2
6  | コンデンサ | 22pF  | 5 | 予備1、赤シールまたはマーカ<sup>[1](#marker)</sup>、色が薄い | C4, C5
7  | ショットキーダイオード |       | 2 |                  | D1
8  | 水晶発振子 | 16MHz | 2 |                  | Y1
9  | MPU      | ATMEGA32U4 | 2 |              | U1
10  | USBコネクタ | Micro Bメス | 4 |           | J1, J2
11 | タクトスイッチ |    | 2 |                  | SW20
12 | スイッチソケット |  | 36 |                 | SW1 - SW18
13 | M2ネジ    | 8mm | 8 |                    |
14 | M2ネジ <sup>[2](#screw)</sup> | 4mm | 8 |                    |
15 | M2樹脂スペーサ | 3mm | 8 |                 |
16 | M2金属スペーサ <sup>[3](#metal_spacer)</sup> | 3.5mm | 8 |                 |
17 | トッププレート |     | 2 |                 |
18 | ボトムプレート |     | 2 |                 |
19 | ゴム足       |      | 10 |                |
20 | USBケーブル  |       | 1 | キーボード間接続用 |

## その他に必要なもの
キットを完成させるためには、以下の部品を別途用意する必要があります。

* キースイッチ（ CherryMX互換のみサポート。ロープロファイルタイプはサポートしていません）
* キーキャップ
* USB Micro B ケーブル（PCとの接続用）

## 作業に必要な工具
組立作業には、最低限以下の工具が必要となります。

* はんだごて（温度調節できるものが望ましい）
* はんだ
* ピンセット
* プラス(+)ドライバ
* ルーペ
* フラックス

その他、必要に応じて以下も用意すると良いです。

* フラックス洗浄剤
* はんだ吸取線
* テスタ

## MPUをつける
1. MPU上に付いている●印と、基板上の○印を合わせて配置します。
2. 4方向全てのピンがパッド上に乗っていることを確認し、はんだ付けします。

![MPU](images/IMG_2794.jpg)

QFPパッケージのはんだ付けは、この[動画](https://www.youtube.com/watch?v=-8SRkSjkZ8A)が参考になるかもしれません。

## 水晶発振子をつける
1. 水晶発振子には取り付ける向きがあります。基板上の部品番号(Y1)の向きと、水晶発振子のパッケージに書かれているマーキングの向きを同じように読み取れるように合わせ、4つのパッドの中心に配置します。
2. 水晶発振子の角に少しだけ端子部分が見えるので、そこをこて先で温めつつはんだを流し込みます。

![Crystal](images/IMG_2796.jpg)

SMDタイプの水晶発振子のはんだ付けは、この[動画](https://www.youtube.com/watch?v=14fJTgFg03M)が参考になるかもしれません。

## 抵抗をつける
1. 抵抗、コンデンサは本当に小さいのであっという間に見失ってしまいます。作業するときは一度に一つずつ、テープから取り出してください。

![Registor](images/IMG_2802.jpg)

## コンデンサをつける
1. コンデンサは部品自体に数値や文字が書かれていないので、値の異なるものを混在させると見た目では識別できなくなりますので、注意してください。

![Capacitor](images/IMG_2803.jpg)

## ショットキーダイオードをつける
1. ダイオードには取り付ける向きがあります。パッケージの片方が白く帯状に塗られている部分を、基板上のダイオードの記号の縦棒の位置に合わせてください。

![Diode](images/IMG_2775.jpg)

## USBコネクタをつける
1. 外側のスルーホール部分ではなく、先に端子部分からはんだ付けするとズレることなく取り付けできます。

![USBConnector](images/IMG_2779.jpg)

## タクトスイッチをつける
1. タクトスイッチは、側面に少しだけ金属の部分が見えていますので、その部分にはんだごてを当てて、ハンダを流し込むようにします。

![TactSwitch](images/IMG_2806.jpg)

## ソケットをつける
1. _ソケットを取り付ける向きが、他と異なる場所が中央付近に２か所(SW7, SW8)あるので注意してください。_
2. 間違った向きに取り付けると、キースイッチを取り付ける真ん中の穴がふさがれてしまいます。
3. まず、全てのソケットの片側だけをはんだ付けしてから、向きを間違えてないか確認し、それから残りの部分をつけると失敗しにくいです。

![Socket](images/IMG_2807.jpg)

## 正しくはんだ付けされているか確認する
回路図( [左側](files/MiniAxeLeft.pdf) 、[右側](files/MiniAxeRight.pdf))を参考に、正しくはんだ付けされているか確認します。

コンピュータに接続する前に、少なくとも以下の項目は確認しましょう。

1. UVCC-GND間、VCCーGND間がショートしていないことを確認します。
2. MPUのピンがブリッジしていないことを確認します。
4. USBコネクタの端子がブリッジしていないこと確認します。


## USBデバイスとして認識されることを確認する
キーボードをコンピュータにつないで、USBデバイスとして認識されることを確認します。

* Macの場合は、「システム情報」を起動して、「ATm32U4DFU」というデバイスが見えているか確認します。
![システム情報](images/system-info.png)

* Windowsの場合は、手元に環境がないので試せていないのですが、デバイスマネージャで「ATm32U4DFU」として見えるようです。

USBデバイスとして認識されない場合は、全ての部品が正しくはんだ付けされているか、回路図を参考に再度確認してください。

## トッププレートをつける
1. M2x8mmネジをトッププレートにはめ込み、マスキングテープ等でネジの頭を固定します。
![トッププレート](images/IMG_2811.jpg)
2. トッププレートを裏返し、樹脂スペーサをつけます。
![樹脂スペーサ](images/IMG_2812.jpg)
3. 基板と組み合わせます。
4. 金属スペーサを基板上に露出しているネジに取り付け、ネジを締めます。
![金属スペーサ](images/IMG_2814.jpg)

## ボトムプレートをつける
1. M3x3mmネジをボトムプレートにはめ込み、基板上の金属スペーサに対して、少しずつ、対角線上のネジを選んで（左上→右下→右上→左下などの順序で）、均等に締め付けていきます。_1本ずつきっちり締め付けていくと、最後のネジが噛み合わなくなることがあるので、注意してください。_

![ボトムプレート](images/IMG_2815.jpg)

## ゴム足をつける
1. ゴム足をボトムプレートにつけます。
![ゴム足](images/IMG_2816.jpg)

## キースイッチとキーキャップ をつける
1. お好みのキースイッチとキーキャップ を取り付けます。 (_Cherry MX互換スイッチのみサポートしています。ロープロファイルタイプはサポートしていませんので、注意してください。_)
2. _キースイッチのピンは曲がりやすいので、まっすぐになっていることを確認してから取り付けてください。また、 SW7とSW8は向きが他とは反対になっているので、注意してください。_

## ファームウェアを書き込む
ファームウェアはQMKを利用します。以下のリポジトリをクローンしてください。

[qmk_firmware](https://github.com/qmk/qmk_firmware)

クローンしたら、ローカルリポジトリのディレクトリへ移動し、以下のコマンドを実行すると、ファームウェアを書き込むために待機状態になりますので、キーボードを接続してください。すでにキーボードが接続されている場合は、そのまま書き込みが始まります。

~~~
$ make miniaxe:default:dfu
~~~

初めてファームウェアを書き込む場合は、リセットスイッチを押す必要はありません。

ファームウェアをビルドする環境の構築は、[こちらのドキュメント](https://docs.qmk.fm/#/getting_started_build_tools)を参考にしてください。

## 完成！
これで完成です。おつかれさまでした。
![Done](images/IMG_2819.jpg)

---

<a name="marker">1</a>: キットによってはマーカで色をつけたものもあります。  
<a name="screw">2</a>: 天キー版では M2 x 3mm が付属していましたが、4mm に変更されました。  
<a name="metal_spacer">3</a>: 天キー版では M2金属スペーサ 3mm が付属していましたが、3.5mm に変更されました。  

