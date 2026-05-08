# TOTEM Keyboard — cjhoare135 Keymap

A custom ZMK firmware configuration for the [TOTEM](https://github.com/GEIGEIGEIST/zmk-config-totem) 38-key split keyboard, based on the [Miryoku](https://github.com/manna-harbour/miryoku) layout with a QWERTY base layer, manually customised to accommodate the additional key per split, that the TOTEM provides.

---

## How it works

- Edit `config/totem.keymap` to change key assignments
- Push your changes to GitHub
- GitHub Actions automatically compiles the firmware
- Download the `.uf2` files from the Actions tab and flash to the keyboard

---

## Key Matrix

The TOTEM has a 3×5 grid plus one outermost key on the bottom row giving 19 keys per split, and 3 thumb keys per side:

```
Left split:                          Right split:
Col:   1     2     3     4     5     6        1     2     3     4     5     6
Row 1:       Q     W     E     R     T        Y     U     I     O     P
Row 2:       A     S     D     F     G        H     J     K     L     '
Row 3: [OUT] Z     X     C     V     B        N     M     ,     .     /     [OUT]
             ESC   SPC   TAB                  RET   BKSP  DEL
```

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
| 7 | Gaming (DayZ) | Combo: RET + BKSP + DEL |
| 8 | Gaming Numbers | Hold TAB (while in Gaming layer) |

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

## Layer 7 — Gaming (DayZ)

**Activated by:** Combo — hold RET + BKSP + DEL together (right thumb cluster)
**Deactivated by:** Same combo again
**Note:** Only the left split is used — right hand is on the mouse

> DayZ notes: Q leans left, E leans right, R reloads, CTRL forces walk, Z is autowalk or collective down when flying, X toggles autohover when flying, G drops held item (hold) or toggles throw action (tap)

```
┌─────┬──────┬─────┬─────┬─────┬─────┐
│     │ CAPS │  Q  │  W  │  E  │  R  │
├─────┼──────┼─────┼─────┼─────┼─────┤
│     │ SHF  │  A  │  S  │  D  │  F  │
├─────┼──────┼─────┼─────┼─────┼─────┤
│  Z  │ CTL  │  X  │  C  │  V  │  M  │
└─────┴──────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐
             │ ESC  │ SPC  │TAB/  │
             │      │      │Nums  │
             └──────┴──────┴──────┘
```

### Key mappings (physical key → DayZ action):

| Physical Key | Sends | DayZ Action |
|---|---|---|
| Outer left (col 1) | Z | Autowalk / collective down when flying |
| Q (col 2, row 1) | CAPS LOCK | Walk/jog toggle |
| W (col 3, row 1) | Q | Lean left |
| E (col 4, row 1) | W | Forward |
| R (col 5, row 1) | E | Lean right |
| T (col 6, row 1) | R | Reload |
| A (col 2, row 2) | SHIFT | Sprint |
| S (col 3, row 2) | A | Strafe left |
| D (col 4, row 2) | S | Backward |
| F (col 5, row 2) | D | Strafe right |
| G (col 6, row 2) | F | Interact |
| Z (col 2, row 3) | CTRL | Force walk |
| X (col 3, row 3) | X | Toggle autohover when flying |
| C (col 4, row 3) | C | Crouch |
| V (col 5, row 3) | G | Drop held item (hold) / toggle throw (tap) |
| B (col 6, row 3) | M | Open map |
| ESC | ESC | Menu |
| SPC | SPC | Jump |
| TAB (tap) | TAB | Inventory |
| TAB (hold) | → Layer 8 | Weapon slots 1-9 |

---

## Layer 8 — Gaming Numbers

**Activated by:** Hold TAB while in Gaming layer
**Used for:** Weapon slot selection in DayZ (1-9)

```
┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │  7  │  8  │  9  │  0  │     │
├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  4  │  5  │  6  │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  1  │  2  │  3  │     │     │
└─────┴─────┴─────┴─────┴─────┴─────┘
             ┌──────┬──────┬──────┐
             │      │      │ [HLD]│
             └──────┴──────┴──────┘
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
