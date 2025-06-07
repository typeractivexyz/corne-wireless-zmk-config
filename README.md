# TyperActiveCorne - ZMK Configuration

This is a customized ZMK configuration for the Corne keyboard with ergonomic features, homerow mods, and multiple layers designed for productivity and comfort.

## Features

- **Homerow Mods**: Modifier keys integrated into the home row for minimal finger movement
- **Multiple Layers**: Base, Navigation, Symbol, System, and Mouse layers
- **Smart Combos**: Efficient keyboard shortcuts and layer toggling
- **Mouse Control**: Full mouse functionality without leaving the keyboard

## Keyboard Layout

![Keyboard layout](keymap.svg)

## Layers

### Default Layer

```
,-----------------------------------------.                    ,-----------------------------------------.        
|      |  Q  |  W  |  E  |  R  |  T  |                    |  Y  |  U  |  I  |  O  |  P  |      |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      |  A  |  S  |  D  |  F  |  G  |                    |  H  |  J  |  K  |  L  | ; : |      |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      |  Z  |  X  |  C  |  V  |  B  |                    |  N  |  M  | , < | . > | / ? |      |
`-----------------------------------------'                    `-----------------------------------------'
         |      |      |      |                              |      |      |      |
         `--------------------'                              `--------------------'
```

- **Home Row (Left)**: A/GUI, S/ALT, D/CTRL, F/SHIFT
- **Home Row (Right)**: J/SHIFT, K/CTRL, L/ALT, ;/GUI
- **Thumb Keys (Left to Right)**: ESC/CTRL, TAB/ALT, ENTER/GUI
- **Thumb Keys (Right to Left)**: SPACE/SYMBOL, BACKSPACE/NAV, DELETE/SYSTEM

### Navigation Layer (Hold Right Backspace)

```
,-----------------------------------------.                    ,-----------------------------------------.        
|      | PREV | C→  | PLAY | NEXT |     |                    |     |     | PgUp | PgDn |     | DEL |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      | HOME |PgDn |PgUp | END |     |                    | ←   |  ↓  |  ↑  |  →  | GUI |     |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      |     |     |     |     | C←  |                    |BR↓  |VOL- |VOL+ |BR↑  |     |     |
`-----------------------------------------'                    `-----------------------------------------'
         |      |      |      |                              |      |      |      |
         `--------------------'                              `--------------------'
```

- **Media Controls**: Previous, Play/Pause, Next
- **Text Navigation**: Home, End, Page Up/Down
- **Arrow Keys**: ←, ↓, ↑, →
- **Screen/Audio**: Brightness and Volume controls

### Symbol Layer (Hold Right Space)

```
,-----------------------------------------.                    ,-----------------------------------------.        
|      |  !  |  @  |  #  |  $  |  %  |                    |  ^  |  &  |  *  |  =  |  -  | PSCR |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      |  ~  |  [  |  {  |  (  |  /  |                    |  \  |  )  |  }  |  ]  |  _  |      |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      |     |  -  |  =  |  `  |  '  |                    |  "  |  -  |  +  |  =  |  |  |      |
`-----------------------------------------'                    `-----------------------------------------'
         |      |      |      |                              |      |      |      |
         `--------------------'                              `--------------------'
```

- **Top Row**: Common symbols used in programming (!@#$%)
- **Middle Row**: Brackets and paired symbols
- **Bottom Row**: Additional symbols for programming and text

### Mouse Layer (Press Tab + Backspace together)

```
,-----------------------------------------.                    ,-----------------------------------------.        
|      | UNDO |      | COPY | PASTE|     |                    | SCL← | SCL↑ |  MUP | SCL↓ | SCL→ |ACCENT|
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      | LGUI | LALT | LCTL | LSFT|     |                    |     | MLFT | MDWN | MRGT | MB3  | TOG |
|------+-----+-----+-----+-----+-----|                    |-----+-----+-----+-----+-----+------|
|      | REDO | ALL  | CUT  |     |     |                    |     | MB4  | MB3  | MB5  |ACCEL |     |
`-----------------------------------------'                    `-----------------------------------------'
         | ESC  | MB2  | MB1  |                              | SCRL | DEL  | MB3  |
         `--------------------'                              `--------------------'
```

- **Mouse Movement**: Arrow keys control pointer (MLFT, MDWN, MUP, MRGT)
- **Mouse Buttons**: 
  - MB1: Left click (right thumb)
  - MB2: Right click (middle thumb)
  - MB3: Middle click (multiple locations for convenience)
- **Scroll Controls**: 4-way scrolling with dedicated directional keys
- **Copy/Paste**: Common clipboard operations on left side
- **Toggle Off**: Press Tab + Backspace again to exit Mouse mode

## Special Features

### Homerow Mods
This keyboard utilizes homerow mods, where holding a key activates a modifier, while tapping it produces the normal letter:

- Left Hand: A(GUI), S(ALT), D(CTRL), F(SHIFT)
- Right Hand: J(SHIFT), K(CTRL), L(ALT), ;(GUI)

### Mouse Layer Toggle
Press Tab + Backspace together to enter or exit the mouse control layer. This allows full control of your pointer without leaving the keyboard.

### Thumb Key Functionality
The thumb keys provide access to common actions and layer switching:

- Tap: Normal key (SPACE, BACKSPACE, etc.)
- Hold: Activate layer or modifier

## File Structure

This configuration uses a special structure for compatibility with the Keymap Editor:

- `corne.keymap` - Main keymap file (compatible with Keymap Editor)
- `behaviors.dtsi` - Custom behaviors definitions
- `layer_defs.dtsi` - Layer constants definitions
- `combos.dtsi` - Combo definitions
- `setup.dtsi` - Main include file for building

## Building

This configuration is designed for ZMK firmware. Use the standard ZMK build process or GitHub workflows to compile the firmware for your Corne keyboard.
