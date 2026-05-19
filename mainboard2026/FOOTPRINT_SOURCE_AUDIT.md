# フットプリント/3Dモデル出典メモ

## 方針

- KiCad公式フットプリントが存在する部品は、KiCad 9.0付属の公式ライブラリ実体へ置換済みです。
- KiCad公式に存在しない `J_RPI1`, `J_MOTDRV1`, `MD1` は、公式図面またはメーカー公式資料に基づく `CANSAT2026` ローカルライブラリとして保持しています。
- 3Dモデルについても、KiCad公式モデルが存在するものは公式STEPモデルを使用しています。ローカル例外部品はプロジェクト内の簡易外形STEP/WRLモデルを追加しています。
- このPCのKiCad 9.0 3Dモデルパッケージで不足していた Raspberry Pi Pico H は、KiCad公式3Dモデルをプロジェクト内にコピーして参照しています。
- XT30U-MはKiCad公式フットプリントを使っていますが、KiCad公式3Dモデルパッケージ側に該当STEPが無いため、プロジェクト内の簡易外形STEP/WRLモデルを使っています。
- `MountingHole` は穴そのものが基板3D形状に反映されるため、個別の部品3Dモデルは設定していません。

## 公式/準公式ソース

- KiCad公式フットプリント: https://gitlab.com/kicad/libraries/kicad-footprints/
- Raspberry Pi 4 Model B 機械図面: https://pip.raspberrypi.com/documents/RP-008343-DS
- SparkFun TB6612FNG ROB-14451 hardware files: https://github.com/sparkfun/Motor_Driver-Dual_TB6612FNG
- Murata OKL-T/6-W12N-C datasheet: https://www.murata.com/-/media/webrenewal/products/power/datasheet/okl-t6-w12.ashx?cvid=20200224053011000000&la=en-sg

## ローカル3Dモデル

| 参照 | モデル | 内容 |
| --- | --- | --- |
| J_RPI1 | `CANSAT2026.3dshapes/RaspberryPi_4B_Model_B_Envelope_Inboard.step` | Raspberry Pi 4Bの85x56mm外形、40ピン位置、固定穴位置を下面側の相手基板として示す簡易外形モデル |
| U_PICO1 | `CANSAT2026.3dshapes/KiCadOfficial/RaspberryPi_Pico_H.step` | KiCad公式3Dモデルのプロジェクト内コピー |
| J_PWR1 | `CANSAT2026.3dshapes/AMASS_XT30U-M_1x02_P5.0mm_Vertical.step` | XT30U-Mの簡易外形モデル |
| J_MOTDRV1 | `CANSAT2026.3dshapes/SparkFun_TB6612FNG_Carrier_2x08_17.78mm.step` | SparkFunキャリア基板の外形、IC、2列ピンヘッダを示す簡易外形モデル |
| MD1 | `CANSAT2026.3dshapes/Murata_OKL-T-6-W12N-C.step` | Murata OKL-T/6-W12N-Cの基板、インダクタ、ピン配置を示す簡易外形モデル |

簡易モデルは衝突確認と実装イメージ確認用です。量産前には実測またはメーカーSTEPが入手できる場合は差し替えてください。
