# Arduino sketches (reorganized)

These sketches were originally a flat dump from before git was used properly.
They are grouped by **what the code does**, with **exact duplicate folders removed**.
Each leaf folder is still a normal Arduino sketch (`Name/Name.ino`).

## Layout

| Folder | What it is |
|--------|------------|
| `ac-soft-starter/` | AC soft-start / phase-angle control: zero-cross interrupt, ramp, current limit, Bluetooth. Evolution from `Controle_AC_simples` through Charles revisions into Kopper+BT finals. |
| `ac-dimmer/` | Simpler pot → delay phase control (`Controle_AC`, `_final`) — same domain, different smaller program. |
| `pwm-senoidal/` | Sine-shaped PWM on pins 5/6 (power-electronics experiment, related to AC drive work). |
| `pid-stepkids/` | STEPKIDS: 2-axis pot → dual DC motors via Victor/servo-style PWM (`PID_Fe*` … `play7_final`). |
| `forca-bianca-aila/` | Despite the `PID_bianca*` names, this is an **LCD + HX711 force/time logger** for “Bianca e Aila” (Newtons, max force/time), not motor PID. |
| `celula-carga/` | Standalone HX711 bring-up (`teste_cell` bit-bang, `celula_de_carga` with library). |
| `dac-osciloscopio/` | Arduino Due DAC0/DAC1 → oscilloscope X–Y vector graphics (`dac` → `dac_vetorial` → circle/arc helpers → commented final). |
| `voz-rgb-bluetooth/` | Bluetooth serial voice commands → RGB LED color names (final = former `__SELECIONADO__…easter_egg`). |
| `a-caixa/` | Teaching platform “A Caixa” (integrated sensors/actuators), with Bluetooth variant. |
| `abre-fecha/` | Door/window open–close with limit switches; `sketch_aug31a` is an early **broken** draft (`void setup {` / `ChaveB`). |
| `fita-led/` | LED strip control (direct + Bluetooth + clap/`palma`). |
| `passo-stepper/` | Stepper motor sketches (test → final → button → interrupt). |
| `carro-voz-servo/` | Differential-drive car on continuous-rotation servos, voice commands over serial. |
| `servo/` | Other servo experiments: sweep test, fair demo loop, light-triggered “sumo”. |
| `libs/HX711master/` | Shared HX711 library (was under `Bibliotecas/`). |

## Exact duplicates removed

| Removed | Identical to |
|---------|----------------|
| `Controle_AC_interrupt` | `Soft_Starter_antes_do_charles` |
| `Soft_Starter_funcionando_14_06` | `Soft_Starter_depois_do_charles` |
| `…_ae_caraia_mod` | `…_ae_caraia` |
| `…_mod_n_snubber` | `…_mod_n` |
| `PID_Fe_play6_testar` | `PID_Fe_play5_mexido` |
| `PID_bianca_comAD_8` | `PID_bianca_comAD_7` |
| `dac_v1` | `dac` |
| `teste_voz_bluetooth` | `voz_bluetooth_simples` |
| `demo` | non-selected `voz_bluetooth_cores_full_com_easter_egg` |
| `AA__SELECIONADO__*` / `__SELECIONADO__*` (PID & DAC) | their non-prefixed finals |
| `voz_bluetooth_cores_demo/` | only `.tmp` garbage files |

Voice RGB **final** kept is the former `__SELECIONADO__voz_bluetooth_cores_full_com_easter_egg` (3 lines ahead of the non-prefixed copy).

## How to open

Open any leaf folder’s `.ino` in the Arduino IDE (or open the family folder and pick a sketch).
