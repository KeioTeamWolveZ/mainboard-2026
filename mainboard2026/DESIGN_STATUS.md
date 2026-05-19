# CanSat 2026 メイン基板 設計メモ

## 現在の状態

- KiCad 9.0で作業を完結する構成です。
- 実部品のフットプリント割り当て、回路図反映、配線、DRC/ERC潰しまで完了しています。
- 3D表示用モデルを設定済みです。KiCadのPCBエディタで `Alt+3` を押すと3Dビューを確認できます。
- Raspberry Pi 4Bは、公式機械図面 RP-008343-DS の85x56mm外形、40ピン位置、4点固定穴を反映したフットプリントへ変更しています。3Dモデルは下面側の相手基板として配置しています。
- Raspberry Pi Picoの3Dモデルは、KiCad公式フットプリント指定どおり `offset (8.89, -24.13, 0)` を適用し、穴/ピン位置を合わせています。
- 余白を減らすため、上面部品は現在の詰めた配置を維持しつつ、Raspberry Pi 4Bの占有域をフットプリント/3Dで明示しました。Pico/モータ系/右側JST群はDRC 0の配置を維持しています。
- 基板外形は `204.47mm x 132.08mm` に詰めた状態を維持し、取付穴もこの外形に合わせて寄せています。
- `exports/` に3Dエクスポートを書き出す運用です。

## 搭載要素

| 機能 | 実装/接続 | 参照 |
| --- | --- | --- |
| Raspberry Pi 4B | 本体外形 + 40-pin GPIO接続 | J_RPI1 |
| モータ用マイコン | Raspberry Pi Pico | U_PICO1 |
| ToFセンサ x2 | 6ピンヘッダ | J_TOF1, J_TOF2 |
| 9軸センサ | 6ピンヘッダ | J_IMU1 |
| GPS | UART 4ピンヘッダ | J_GPS1 |
| LoRa | UART 7ピンヘッダ | J_LORA1 |
| SDカード | SPI接続ヘッダ | J_SD1 |
| モータドライバ | SparkFun TB6612FNG carrier | J_MOTDRV1 |
| モータ/サーボ/分離機構 | JST-XH | J_MOTOR_A, J_MOTOR_B, J_SERVO1, J_SEP1 |
| 12V入力 | XT30 | J_PWR1 |
| 12V to 5V降圧 | Murata OKL-T/6-W12N-C | MD1 |
| 分離機構スイッチ | TO-252 MOSFET + 抵抗 | Q1, R_SEP_G, R_SEP_PD |

## 最終検証

- PCB DRC: 0 violations / 0 unconnected
- 回路図 ERC: 0 violations
