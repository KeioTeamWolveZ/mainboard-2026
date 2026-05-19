# フットプリント割り当て

KiCad公式ライブラリに存在する部品はKiCad公式フットプリントを使用しています。KiCad公式に存在しない部品/基板外形だけ、公式図面またはメーカー公式資料に基づくプロジェクト内フットプリントを使用しています。

| 参照 | 用途 | フットプリント | 出典 |
| --- | --- | --- | --- |
| J_RPI1 | Raspberry Pi 4B本体外形 + 40-pin GPIO | `CANSAT2026:RaspberryPi_4B_40pin_Mount` | KiCad公式なし。Raspberry Pi公式機械図面 RP-008343-DS 準拠 |
| U_PICO1 | Raspberry Pi Pico | `Module:RaspberryPi_Pico_Common_THT` | KiCad公式 |
| J_TOF1/J_TOF2 | VL53L1X ToFセンサ接続 | `Connector_PinHeader_2.54mm:PinHeader_1x06_P2.54mm_Vertical` | KiCad公式 |
| J_IMU1 | BNO085 9軸センサ接続 | `Connector_PinHeader_2.54mm:PinHeader_1x06_P2.54mm_Vertical` | KiCad公式 |
| J_SD1 | microSD SPI breakout接続 | `Connector_PinHeader_2.54mm:PinHeader_1x07_P2.54mm_Vertical` | KiCad公式 |
| J_LORA1 | Ebyte E220 UART LoRa接続 | `Connector_PinHeader_2.54mm:PinHeader_1x07_P2.54mm_Vertical` | KiCad公式 |
| J_MAG_STAB/J_MAG_MOD | マグネット/ポゴ接続 | `Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical` | KiCad公式 |
| J_GPS1 | UART GPS接続 | `Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical` | KiCad公式 |
| J_MOTOR_A/J_MOTOR_B | モータ出力 | `Connector_JST:JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical` | KiCad公式 |
| J_SERVO1 | サーボ出力 | `Connector_JST:JST_XH_B3B-XH-A_1x03_P2.50mm_Vertical` | KiCad公式 |
| J_SEP1 | 分離機構出力 | `Connector_JST:JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical` | KiCad公式 |
| J_PWR1 | 12V入力 | `Connector_AMASS:AMASS_XT30U-M_1x02_P5.0mm_Vertical` | KiCad公式 |
| Q1 | IRLR7843PbF low-side MOSFET | `Package_TO_SOT_SMD:TO-252-3_TabPin2` | KiCad公式 |
| R_MAG/R_TRIM1/R_SEP_G/R_SEP_PD | 抵抗 | `Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P2.54mm_Vertical` | KiCad公式 |
| MH1-MH4/MH_CAM1-MH_CAM2 | 取付穴/カメラケーブル保持穴 | `MountingHole:MountingHole_2.5mm` | KiCad公式。穴なので3D部品モデルなし |
| J_MOTDRV1 | SparkFun TB6612FNG carrier | `CANSAT2026:SparkFun_TB6612FNG_Carrier_2x08_17.78mm` | KiCad公式なし。SparkFun公式基板寸法準拠 |
| MD1 | Murata OKL-T/6-W12N-C buck | `CANSAT2026:Murata_OKL-T-6-W12N-C` | KiCad公式なし。Murata公式データシート寸法準拠 |
