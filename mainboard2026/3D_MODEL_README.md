# 3D基板化メモ

## KiCadでの確認

1. `cansat_2026_mainboard_kicad9.kicad_pro` をKiCad 9.0で開きます。
2. PCBエディタを開きます。
3. `Alt+3` で3Dビューを開きます。

## モデル構成

- KiCad公式フットプリントは、原則としてKiCad付属の公式STEPモデルを参照しています。
- Raspberry Pi 4Bは下面側に接続される相手基板として簡易STEP/WRLモデルを配置しています。
- このPCのKiCad 9.0に不足していたPico Hの公式STEPは、プロジェクト内 `CANSAT2026.3dshapes/KiCadOfficial/` にコピーして参照しています。
- `J_RPI1`, `J_MOTDRV1`, `MD1`, `J_PWR1` は `CANSAT2026.3dshapes/` に簡易外形STEP/WRLモデルを追加しています。
- 取付穴は基板穴として3D出力されるため、別モデルはありません。

## 生成物

- `exports/cansat_2026_mainboard_kicad9.glb`: 3D確認・共有向け
- `exports/cansat_2026_mainboard_kicad9.step`: 機械CAD連携向け
- `exports/cansat_2026_mainboard_kicad9.wrl`: KiCad/VRML互換確認向け
