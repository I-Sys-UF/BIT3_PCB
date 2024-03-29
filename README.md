# BIT3_PCB

KiCad 7.0.x にて設計

# BIT とは

**B**eginning **I**.Sys **T**racer のイニシャルで、新入生教育用のライントレーサの筐体です  
先代の BIT2 の設計を踏襲しつつ、マイコンを RP2040 搭載の秋月製 AE-2040 に置き換えました。ギアボックス等は流用できるようにしています

# 部品表

## 主要部品

| 部品番号 | 部品名 | 秋月 |
|:----|:----|:----|
| R1 - R5 | 100 Ω | [R-25101](https://akizukidenshi.com/catalog/g/gR-25101/) |
| R6 - R10 | 47 k Ω | [R-25473](https://akizukidenshi.com/catalog/g/gR-25473/) |
| R12 - R16 | 510 Ω | [R-25511](https://akizukidenshi.com/catalog/g/gR-25511/) |
| R11、R17 - R21 | 1k Ω | [R-25102](https://akizukidenshi.com/catalog/g/gR-25102/) |
| C1 - C3 | 0.1 uF | [P-10147](https://akizukidenshi.com/catalog/g/gP-10147/) |
| D1 - D5 | 5mm LED | [I-13172](https://akizukidenshi.com/catalog/g/gI-13172/) |
| D6 | 1N4148 | [I-00941](https://akizukidenshi.com/catalog/g/gI-00941/) |
| U1 | AE-RP2040 | [K-17542](https://akizukidenshi.com/catalog/g/gK-17542/) |
| U2 - U6 | LBR-127HLD | [P-04500](https://akizukidenshi.com/catalog/g/gP-04500/) |
| U7 | MCP3008 | [I-09485](https://akizukidenshi.com/catalog/g/gI-09485/) |
| U7 | IC ソケット | [P-00007](https://akizukidenshi.com/catalog/g/gP-00007/) |
| U8 | AE-DRV8835 | [K-09848](https://akizukidenshi.com/catalog/g/gK-09848/) |
| U9 | NJM7805FA | [I-08678](https://akizukidenshi.com/catalog/g/gI-08678/) |
| Q1 | 2SC1815 | [I-17089](https://akizukidenshi.com/catalog/g/gI-17089/) |
| F1 | リセッタブルヒューズ | [P-12628](https://akizukidenshi.com/catalog/g/gP-12628/) |
| SW1 | 電源スイッチ | [P-00300](https://akizukidenshi.com/catalog/g/gP-00300/) |
| EXEC, MODE | タクタイルスイッチ | [P-03647](https://akizukidenshi.com/catalog/g/gP-03647/) |
| J1 | 2 列ピンヘッダ | [C-00080](https://akizukidenshi.com/catalog/g/gC-00080/) |
| J2 | バッテリ接続用ケーブル・コネクタ | 省略 |
| J3, U1 | 1 列ピンソケット | [C-05779](https://akizukidenshi.com/catalog/g/gC-05779/) |

## その他の部品

| 部品名 | 商品名 | リンク |
|:----|:----|:----|
| 前輪 | タミヤ　ボールキャスター | <https://tamiyashop.jp/shop/g/g70144> |
| 動力 | タミヤ　ダブルギヤボックス（左右独立4速タイプ） | <https://tamiyashop.jp/shop/g/g70168> |
| 後輪 | タミヤ　スリムタイヤセット | <https://tamiyashop.jp/shop/g/g70193> |
| XBee | XBee S2C ワイヤアンテナ型 | <https://www.switch-science.com/products/4089> |
| XBee 用変換基板 | XBeeエクスプローラ5Vマイコン用 | <https://www.switch-science.com/products/1166> |
| XBee 用 USB アダプタ | XBeeエクスプローラUSBドングル | <https://www.switch-science.com/products/1790> |

# 回路図

![BIT3＿Schematic](./img/BIT3.svg)

# 基板デザイン

![BIT3＿PCB](./img/BIT3_PCB_Design.png)

# 更新履歴

- `v1.0`
  - 初回リリース
- `v1.1`
  - ADC にバッテリ電圧が直接入力される問題を修正
- `v1.2`
  - 接続されていない GND ベタが存在する問題を修正
- `v1.3`
  - モータ・ドライバに電源が供給されていない問題を修正
- `v1.4`
  - ADC IC MCP3008 にパスコンを追加
- `v1.5` 
  - 前輪と部品が微妙に干渉する問題を修正
- `v1.6`
  - 逆接防止ダイオードの追加、バッテリ入力の接続の変更、一部部品の変更（基板には影響なし）
- `v1.7`
  - フォトセンサを変更
- `v2.0`
  - XBee 接続用のコネクタを追加
- `v2.1`
  - BACK を EXEC に変更

# ライセンス

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">クリエイティブ・コモンズ 表示 - 非営利 - 改変禁止 4.0 国際 ライセンス</a>の下に提供されています。

利用を希望される方は部の[公式 Twitter ](https://twitter.com/ISys_robocon)までご連絡ください
