## ZebraプリンタとWindows PCをシリアル接続する方法

Zebra プリンタとホスト機器をシリアル接続するご要望は一定するある。

- PLC <> Printer
- PC <> Printer
- Iot Device <> Printer
- Scanner <> Printer

<br>

接続先のプリンタ機種によって、コネクタ形状が異なる。ホストとコネクタに合った接続ケーブルを用意すること。

| Printer | Connector Type   |
| ------- | ---------------- |
| ZT      | Dsub9(Female)    |
| ZD      | Dsub9(Female)*   |
| ZQ6     | Dsub9(特殊コネクタ） |
| ZQ6以外 | なし             |

\* Dsub9 I/Fがついている機種を選択すること。

<br>

参考までにWindows PCとZT/ZDプリンタをシリアル接続し、データを送受信する方法について記載する。

1. 準備するもの（推奨）

    - Windows 10以上のPC
    - ZT/ZDプリンタ (Dsub9ピンがあるもの)
    - USBシリアル変換ケーブル（[BSUSRC07シリーズ](https://www.buffalo.jp/product/detail/bsusrc0710bs.html)）
    - Dsub9 クロスケーブル オス-メス

    <br>

1. USBシリアル変換ケーブルのドライバをインストールして、利用できるようにしておく。
    <br>
    

1. Device Managerでポート番号を確認する。
    ![1747294492462](image/README/1747294492462.png)
    <br>
    

1. TeraTermをインストールする。
    https://github.com/TeraTermProject/teraterm/releases
    <br>
    

1. Teratermを起動する。
    シリアル > USBx: Serial Port (Comx)
    ※ 先に調べたComポート番号を選択する。

    ![1747294721104](image/README/1747294721104.png)
    <br>
    

1. 設定＞端末

    - 送信 : CR+LF
    - ローカルエコー : チェック

    ![1747294839967](image/README/1747294839967.png)
    <br>
    

1. OKを選択し、設定画面を閉じる。
    <br>
    

1. ~HSを送信し、通信可否を確認する。

    ![1747295017901](image/README/1747295017901.png)

以上