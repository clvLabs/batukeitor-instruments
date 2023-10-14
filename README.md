# Batukeitor instruments

This repo contains definitions, audio samples and icons for instruments to be used with [Batukeitor](https://github.com/clvLabs/batukeitor).

## The `instruments.yml` file

This file contains de definitions of all instruments.

```yml
# Batukeitor instruments file
instruments:

  MT:
    name: "Metrónomo"
    samples:
      "X": "MT_hi.mp3"
      "-": "MT_lo.mp3"
      "1": "MT_hi.mp3"
      "2": "MT_lo.mp3"
      "3": "MT_lo.mp3"
      "4": "MT_lo.mp3"
      "5": "MT_lo.mp3"
      "6": "MT_lo.mp3"
      "7": "MT_lo.mp3"
      "8": "MT_lo.mp3"

  #(...more content...)

  TB:
    name: "Tamborim"
    samples:
      "X": "TB_hi.mp3"
      "-": "TB_lo.mp3"

  RP:
    name: "Repenique"
    samples:
      "X": "RP_Baqueta_Centro.mp3"
      "x": "RP_Baqueta_Aro.mp3"
      "-": "RP_Palma_Abierta.mp3"
      ".": "RP_Palma_Cerrada.mp3"

  #(...more content...)

  S1:
    name: "Surdo 1ª"
    samples:
      "X": "S1_hi.mp3"
      "-": "S1_lo.mp3"
```

## Structure of a single `instrument`
Each instrument is defined by an `instrument block`:
```yml
  RP:
    name: "Repenique"
    samples:
      "X": "RP_Baqueta_Centro.mp3"
      "x": "RP_Baqueta_Aro.mp3"
      "-": "RP_Palma_Abierta.mp3"
      ".": "RP_Palma_Cerrada.mp3"
```

In this case, the instrument's `id` (identificator) is `RP`, its `name` is `Repenique` and it has different `samples` (notes):
* `X`: Drumstick on center (file: `RP_Baqueta_Centro.mp3`)
* `x`: Drumstick on edge (file: `RP_Baqueta_Aro.mp3`)
* `-`: Open palm (file: `RP_Palma_Abierta.mp3`)
* `.`: Closed palm (file: `RP_Palma_Cerrada.mp3`)

These notes can be used later to write scores.

You can add as many `samples` as you want to each instrument... if you have a good collection of audio samples you can give your scores very detailed info about the sound you want to achieve in your compositions.

The instrument `identificators` can be changed, as long as you use the same in the `tracks` of your scores. The only exception is the `MT` (_Metrónomo_), wich is used in the code (if you want to change the code as well, then there's no exceptions!).

## The `img` folder
This folder should contain a `png` file for each instrument `id`.

## The `samples` folder
This file should contain all audio files specified in the `samples` sections of the instruments.
