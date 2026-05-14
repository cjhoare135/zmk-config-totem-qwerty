# TOTEM Keyboard — cjhoare135 Keymap

A custom ZMK firmware configuration for the [TOTEM](https://github.com/GEIGEIGEIST/zmk-config-totem) 38-key split keyboard. QWERTY base with Miryoku-style layers and home row mods.

---

## How it works

- Edit `config/totem.keymap` to change key assignments
- Push your changes to GitHub
- GitHub Actions automatically compiles the firmware
- Download the `.uf2` files from the Actions tab and flash to the keyboard

---

## Keymap Reference

[![TOTEM Keymap Reference](docs/keymap_reference.png)](docs/totem_keymap_reference.html)

[Interactive HTML reference](docs/totem_keymap_reference.html)

---

## Layers

| # | Name | Activated by |
|---|------|-------------|
| 0 | Base (QWERTY) | Default |
| 1 | Numbers | Hold BKSP |
| 2 | Symbols | Hold RET |
| 3 | Media | Hold ESC |
| 4 | Navigation | Hold SPC |
| 5 | Mouse | Hold TAB |
| 6 | Function | Hold DEL |

---

## Layer 0 — Base (QWERTY)

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │A/META│S/ALT│D/CTL│F/SHF│  G  │   │  H  │J/SHF│K/CTL│L/ALT│'/META│     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│  ←  │  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │  →  │
└─────┴─────┴─────┴─────┴─────┴─────┘   └─────┴─────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │ESC/  │SPC/  │TAB/  │         │RET/  │BKSP/ │DEL/  │
             │Media │Nav   │Mouse │         │Sym   │Num   │Func  │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

> Home row mods: tap for the letter, hold for the modifier shown after /
> Outer keys (col 1): left = ← arrow, right = → arrow
> Use with Meta for workspace switching: Meta+← / Meta+→

---

## Layer 1 — Numbers

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │  [  │  7  │  8  │  9  │  ]  │   │     │     │     │     │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  ;  │  4  │  5  │  6  │  =  │   │     │ SHF │ CTL │ ALT │ META │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  `  │  1  │  2  │  3  │  \  │   │     │     │     │     │     │     │
└─────┴─────┴─────┴─────┴─────┴─────┘   └─────┴─────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │  .   │  0   │  -   │         │      │ [HLD]│      │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Layer 2 — Symbols

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │  {  │  &  │  *  │  (  │  }  │   │     │     │     │     │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  :  │  $  │  %  │  ^  │  +  │   │     │ SHF │ CTL │ ALT │ META │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  ~  │  !  │  @  │  #  │  |  │   │     │     │     │     │     │     │
└─────┴─────┴─────┴─────┴─────┴─────┘   └─────┴─────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │  (   │  )   │  _   │         │ [HLD]│      │      │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Layer 3 — Media

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌──────┬──────┬──────┬──────┬──────┬─────┐
│     │     │     │     │     │     │   │BT_CLR│      │      │BT_PRV│BT_NXT│     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│     │ META │ ALT │ CTL │ SHF │     │   │ PWR  │ PREV │ VOL- │ VOL+ │ NEXT │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│BT   │     │     │     │     │     │   │ OUT  │ BT0  │ BT1  │ BT2  │ BT3  │ BT4 │
│CLR  │     │     │     │     │     │   │ TOG  │      │      │      │      │     │
└─────┴─────┴─────┴─────┴─────┴─────┘   └──────┴──────┴──────┴──────┴──────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │ [HLD]│      │      │         │ STOP │ PLAY │ MUTE │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Layer 4 — Navigation

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌──────┬──────┬──────┬──────┬──────┬─────┐
│     │     │     │     │     │     │   │ REDO │PASTE │ COPY │ CUT  │ UNDO │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│     │ META │ ALT │ CTL │ SHF │     │   │ CAPS │  ←   │  ↓   │  ↑   │  →   │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│     │     │     │     │     │     │   │ INS  │ HOME │ PGDN │ PGUP │ END  │     │
└─────┴─────┴─────┴─────┴─────┴─────┘   └──────┴──────┴──────┴──────┴──────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │      │ [HLD]│      │         │      │      │      │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Layer 5 — Mouse

```
┌─────┬─────┬─────┬─────┬─────┬─────┐   ┌──────┬──────┬──────┬──────┬──────┬─────┐
│     │     │     │     │     │     │   │ REDO │PASTE │ COPY │ CUT  │ UNDO │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│     │ META │ ALT │ CTL │ SHF │     │   │      │  ←   │  ↓   │  ↑   │  →   │     │
├─────┼─────┼─────┼─────┼─────┼─────┤   ├──────┼──────┼──────┼──────┼──────┼─────┤
│     │     │     │     │     │     │   │      │ SCL← │ SCL↓ │ SCL↑ │ SCL→ │     │
└─────┴─────┴─────┴─────┴─────┴─────┘   └──────┴──────┴──────┴──────┴──────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │      │      │ [HLD]│         │ LCLK │ MCLK │ RCLK │
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Layer 6 — Function

```
┌─────┬─────┬─────┬─────┬───────┬───────┐   ┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │ F12 │  F7 │  F8 │   F9  │ PRTSC │   │     │     │     │     │     │     │
├─────┼─────┼─────┼─────┼───────┼───────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │ F11 │  F4 │  F5 │   F6  │ SCRLK │   │     │ SHF │ CTL │ ALT │ META │     │
├─────┼─────┼─────┼─────┼───────┼───────┤   ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │ F10 │  F1 │  F2 │   F3  │ PAUSE │   │     │     │     │     │     │     │
└─────┴─────┴─────┴─────┴───────┴───────┘   └─────┴─────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐         ┌──────┬──────┬──────┐
             │ META │ SPC  │ TAB  │         │      │      │ [HLD]│
             └──────┴──────┴──────┘         └──────┴──────┴──────┘
```

---

## Flashing the keyboard

1. Go to the [Actions tab](../../actions) on GitHub
2. Click the latest successful build and scroll down to **Artifacts**
3. Download and unzip `firmware.zip`
4. Connect the **left half** to your PC and double-tap the reset button — it will appear as a USB drive
5. Drag and drop `totem_left-seeeduino_xiao_ble-zmk.uf2` onto it
6. Repeat with the **right half** and `totem_right-seeeduino_xiao_ble-zmk.uf2`

---

## Resources

- [ZMK Documentation](https://zmk.dev/docs)
- [ZMK Keycodes](https://zmk.dev/docs/codes)
- [TOTEM keyboard](https://github.com/GEIGEIGEIST/zmk-config-totem)
- [Miryoku layout](https://github.com/manna-harbour/miryoku)
