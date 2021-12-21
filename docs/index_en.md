# GRIN Type-R 組み立て手順

## Introduction

Thank you for your purchase of GRIN Type-R. This kit requires soldering and firmware writing. Please follow the steps below to assemble.

## Precautions

This product is compatible with Cherry MX switches and compatible products. Keycaps are assumed to be 19mm pitch and 18mm square, but we cannot guarantee compatibility.  
TBD: List of confirmed compatible keycaps

## Heading

1. Preparation
2. Confirmation of kit contents
3. Initial operation check
4. Soldering the diode
5. Soldering the PCB socket for the switch
6. Install the stabilizer
7. Screw the switch plate to the PCB
8. Install the switch
9. Attach the top plate and PCB
10. Attach the feet to the bottom plate
11. Attach the bottom plate.
12. Attach the key cap.
13. Operation check
A1. Appendix

## 1. Preparation

### Deciding the Layout
GRIN Type-R allows you to choose the combination of ANSI, ISO, JIS, single space bar and split space bar. Since the number of switches and keycaps required for each type of layout varies, it is necessary to decide the layout in advance.

![layout](https://user-images.githubusercontent.com/3132296/138850765-6f6eb771-3ea8-43cc-b2cc-f62aec732313.png)

### Prepare the parts required in addition to the kit
- Keycaps (Cherry MX compatible) ... * Match the selected layout.  
[YUSHAKOBO](https://shop.yushakobo.jp/collections/keycaps)  
[TALP KEYBOARD](https://talpkeyboard.net/?category_id=59be183f428f2d49120007b1)  
- Key switch (Cherry MX compatible) ... * Match to the selected layout.  
[YUSHAKOBO](https://shop.yushakobo.jp/collections/all-switches)  
[TALP KEYBOARD](https://talpkeyboard.net/?category_id=59cf8860ed05e668db003f5d)  
- PCB socket for Cherry MX switch ... * Match the selected layout.  
Not required if you want to install the keyswitch directly.  
[YUSHAKOBO](https://shop.yushakobo.jp/products/a01ps)  
[TALP KEYBOARD](https://talpkeyboard.net/items/5e02c5405b120c792616bcf9)  
- Stabilizer (PCB mount) ... * Match the selected layout  
[YUSHAKOBO](https://shop.yushakobo.jp/products/a0500st?variant=37665699430561)  
[TALP KEYBOARD](https://talpkeyboard.net/?category_id=5f884b9b3313d216eb50558a)  
- Wire for 3U stabilizer ... * Match the selected layout.  
This is required when using a space bar that is not split. The size of the wire is not common, so please make your own or purchase separately from Yushakobo.  
[YUSHAKOBO](https://shop.yushakobo.jp/products/a0500st?variant=40429698678945)
- USB Type-C cable (for data communication) ... 1pc  
- Micro USB cable (for data communication) ... 1pc  
To check Pico's operation.

### Prepare the tools
- はんだごて（電子基板用）
- はんだ
- フラックス
- フラックスクリーナー（IPA等のアルコールや溶剤でも代用可能）
- ピンセット
- ニッパー
- プラスドライバー(No.0)
- ティッシュ

### 他にあるといい物
- シリコン作業マット
- ウエス、キムワイプ、綿棒
- マスキングテープ
- はんだ吸い取り線、はんだ吸い取り器
- テスター(トラブル時の原因調査用)

## ２．キット内容の確認
以下が揃っていることをご確認ください。
不足がある場合は、Boothショップサイトのトップページ上部にある、メールアイコンよりメッセージを下さい。
- 基板(PCB) … 1枚  
- トッププレート(FR-4) … 1枚  
- スイッチプレート(アルミ) … 1枚  
- ボトムプレート(FR-4) … 1枚  
- 袋➀  
    - ダイオード(1N4148) … 75個
- 袋➁  
    - M2ネジ(銀) … 6個
    - スペーサー短(丸型両メネジ) … 3個  
- 袋➂  
    - M2ネジ(黒) … 16個  
    - スペーサー長(丸型両メネジ) … 8個  
    - スペーサー太(丸型中空) … 8個  
- 袋➃  
    - プラワッシャー … 8個  
    - ゴムワッシャー … 24個  
- 袋➄  
    - アルミ足 … 2個
    - M4ネジ … 2個
    - ゴム足 … 2個

## ３．初期動作確認

出荷状態の基板はKMK Firmwareが書き込み済みになっています。先ず正常動作することを確認します。

### PCに接続し認識されることを確認する

USBケーブルで基板とPCを接続します。「CIRCUITPY」というドライブが認識されることを確認します。

### ピンセット等で端子を短絡させ入力されることを確認する

![IMG_20211024_184022__01](https://user-images.githubusercontent.com/3132296/138600349-d7a1206c-a3c7-4663-90a5-6ad1bfbf6f9c.jpg)  
ピンセット等の導体で写真の2点を短絡して「1」が入力されることを確認してください。入力されない場合は、Boothショップサイトのトップページ上部にある、メールアイコンよりメッセージを下さい。

※出荷状態ではキー配列がUS配列単体スペースバーになっています。

## ４．ダイオードのはんだ付け

注意！  
キー配列およびスイッチの取り付け方法によってダイオードの取り付けが不要な位置があります。  
不要な位置にダイオードを取り付けるとスタビライザーと干渉する可能性があるため取り付けないで下さい。  
- ２Uバックスペースの場合  
D15不要  
- ISOエンター(直付け)の場合  
D45不要  
- ISOエンター(ソケット)の場合  
D30不要  
- 2.25Uエンターの場合  
D44不要  
- 2.25U左シフトの場合  
D48不要  
- 2U右シフトの場合  
D60不要  
- 2.75Uスペースバーの場合  
D66、D68不要  
- 3Uスペースバーの場合  
D66、D68不要  
- スプリットスペースの場合  
D67不要  

ダイオードの足を曲げます。  
![IMG_20211024_185426__01](https://user-images.githubusercontent.com/3132296/138599397-515d71bd-303b-48e0-98fb-fd6c56f75fc6.jpg)

シルクの向きとダイオードの向きを合わせてセットします。  
![IMG_20211024_185451__01](https://user-images.githubusercontent.com/3132296/138599443-0b524bb9-5166-402d-975e-d0db50a08e34.jpg)

ダイオードをマスキングテープで固定します。  
![IMG_20211024_185700__01](https://user-images.githubusercontent.com/3132296/138599491-e0bae086-d260-48b1-b428-10e3a5f24a5f.jpg)

裏返してはんだ付けします。  
![IMG_20211024_185829__01](https://user-images.githubusercontent.com/3132296/138599533-31aaaf06-3e98-4a53-ac3d-a49286c5c794.jpg)

足をニッパーで切断し、フラックスクリーナーで周囲を奇麗にします。  
![IMG_20211024_190343__01](https://user-images.githubusercontent.com/3132296/138599571-aa82a8cc-f0f4-4994-95de-8e2329e0151e.jpg)

## ５．スイッチ用PCBソケットのはんだ付け

※注意 スイッチを直付けする場合、この項の手順は飛ばして下さい。

ソケットを配置してはんだ付けします。浮かないようにピンセットで押さえながらはんだ付けして下さい。  
![IMG_20211024_191023__01](https://user-images.githubusercontent.com/3132296/138601716-b302675a-c47f-4df0-85e3-4094c506b9ff.jpg)

※向きに注意　下の写真の向きは間違いです。  
![IMG_20211024_190934__01](https://user-images.githubusercontent.com/3132296/138602574-db98be8a-e68b-4710-9918-185e2c19d15a.jpg)

## ６．スタビライザーの取り付け

2U以上のサイズのバックスペース、シフトキー、エンターキーおよびISOエンターのために2Uスタビライザーを取り付けます。  
![IMG_20211024_201044__01](https://user-images.githubusercontent.com/3132296/138602682-9a904d91-1ccc-49bf-b053-58f890d8d942.jpg)

3Uスペースバーには3Uワイヤーのスタビライザーを取り付けます。  

## ７．スイッチプレートと基板のねじ止め

袋➁のネジとスペーサーで基板とスイッチプレートを3か所ねじ止めします。  
![IMG_20211025_012308](https://user-images.githubusercontent.com/3132296/138603250-d2de6202-2906-4cfb-a936-b46ea861370a.jpg)

![IMG_20211024_202016__01](https://user-images.githubusercontent.com/3132296/138603264-aa535f03-cefc-45b1-8bed-a865e45260f8.jpg)

## ８．スイッチの取り付け

ソケットの場合は、スイッチの端子を曲げないように気を付けてスイッチを刺して下さい。  
直付けの場合は、裏からはんだ付けして下さい。その際、スイッチが浮かないように気を付けて下さい。  
![IMG_20211024_204917__01](https://user-images.githubusercontent.com/3132296/138603407-edfcd077-62f7-4b1f-a821-9fadd0bea6f5.jpg)

## ９．トッププレートと基板の取り付け

袋➂のネジとスペーサー長をトッププレートに8か所取り付けます。  
![IMG_20211024_211905__01](https://user-images.githubusercontent.com/3132296/138603512-0a3e8f68-802c-4a07-bf53-0dec95cf8f33.jpg)

袋➃のプラワッシャーを1枚ずつスペーサーに刺します。次に袋➃のゴムワッシャを1枚ずつスペーサーに刺します。  
![IMG_20211024_211924__01](https://user-images.githubusercontent.com/3132296/138603569-339cebf9-9d9b-4629-9fc4-827d561a5353.jpg)

基板とねじ止めしたスイッチプレートをスペーサーに刺します。  
![IMG_20211024_212044__01](https://user-images.githubusercontent.com/3132296/138603678-1e5cce81-fcb9-41f5-9264-fee6a1c8ebae.jpg)

袋➃のゴムワッシャを"2"枚ずつスペーサーに刺します。次に袋➂のスペーサー太を刺します。  
![IMG_20211024_212158__01](https://user-images.githubusercontent.com/3132296/138603821-a8e88bc6-4702-40da-89e2-c6be5727c03e.jpg)  
スペーサーの面がつらいちにならない場合、スペーサーの枚数や浮きを確認して下さい。  

## １０．ボトムプレートに足を取り付け

袋➄のアルミ足とゴム足をボトムプレートに取り付けます。  
アルミ足はM4ネジでボトムプレートに取り付けます。
赤丸はゴム足の貼り付け位置です。  
![IMG_20211025_014513](https://user-images.githubusercontent.com/3132296/138604792-a759b5c9-d56e-4aab-8051-d91510aab9e7.jpg)

## １１．ボトムプレートの取り付け

袋➂のネジで本体とボトムプレートを8か所ねじ止めします。

## １２．キーキャップの取り付け

スイッチにキーキャップを取り付けます。

## １３．動作確認

USBケーブルでPCと接続し動作確認します。必要であればソースコードを修正しキー配列を修正します。
※執筆中

## Ａ１．付録

トラブルシュートおよびファームウェアの改造にお役立て下さい。  

### USBストレージの無効化 　

boot.pyを以下の内容に書き換えてください。USBを挿抜して再接続するとUSBストレージが認識されなくなります。  
注意! 不用意に修正するとREPLから復旧するか、ファームウェアを再インストールする必要があります。  

boot.py
```
import storage
import supervisor

storage.disable_usb_drive()
supervisor.set_next_stack_limit(4096 + 4096)
```

### USBストレージの再有効化 　

[MU Editorダウンロード](https://codewith.mu/en/download)  
インストールしてください。  

GRIN Type-RをPCに接続します。  
Mu Editorを起動します。  
ツールバーからシリアルボタンをクリックします。  
![mu1](https://user-images.githubusercontent.com/3132296/139570715-863a8d0e-bd0e-4078-bd58-74653904e181.png)

REPLペインをクリックし「Ctrl+C」を押下します。  
![mu2](https://user-images.githubusercontent.com/3132296/139570725-34043950-0abd-4ff3-8fd7-a7b0392efc4c.png)

「Enter」を押下します。  
![mu3](https://user-images.githubusercontent.com/3132296/139570730-8251d9de-786d-4ed5-adbd-70f82e0f3e97.png)

以下のコードを直接コピー＆ペーストします。（手入力ではなく）  
```
import os
import storage
storage.remount('/', readonly=False)
os.remove('boot.py')
```

![mu4](https://user-images.githubusercontent.com/3132296/139570737-318f5c8b-f691-4309-be04-386b7738ed17.png)

GRIN Type-RのUSBを挿抜して再接続するとUSBドライブとして認識するようになります。  
ドライブからboot.pyが消えているため以下のコードでboot.pyを作成します。  

boot.py
```
import supervisor

supervisor.set_next_stack_limit(4096 + 4096)
```

### 回路図  
![schematic](https://user-images.githubusercontent.com/3132296/139060252-92dcc313-b126-41d9-8f86-858f542e6534.jpg)

### Circuit Pythonで問題が発生した時のヒント  
https://learn.adafruit.com/welcome-to-circuitpython/troubleshooting
