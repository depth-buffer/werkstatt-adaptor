# werkstatt-adaptor
Moog Werkstatt-01 filter feedback &amp; Eurorack adaptor

## What is it?

A design for a circuit that makes it easier to use in conjunction with Eurorack
modular synths, as well as adding VCF feedback in the style of the original
Minimoog filter feedback trick.

Features:
* Three input mixer designed to mix the Werkstatt's VCO, an external Eurorack
  audio signal, and the output of the Werkstatt's filter
  * Includes final mix attenuator/amplifier
  * VCO and external inputs are AC coupled
  * Mixed output can be fed into Werkstatt VCF audio in
* AC coupled level booster (gain 1.68) to make it easier to use VCO or VCF
  direct output in a Eurorack system
* AC coupled level booster (gain 3) to make it easier to use the Werkstatt's
  final audio output in a Eurorack system
* Small BOM, using a single TL074 IC

## How?

Other than the adaptor itself, which you will have to build, the only other
requirements are a Werkstatt-01 with CV Expander. To use the input mixer as
intended, you will need to perform the VCO output normal mod: cut or remove
JMP57 on the Werkstatt-01 main board, and solder a wire jumper to JMP1 on the
CV Expander board. Without this mod performed, the internal VCO is permanently
routed to the VCF, and summed with anything patched into VCF AUD IN. After this
mod, the VCO is _normalled_ to the VCF; i.e. the VCO feeds into the VCF by
default, but once something is patched into VCF AUD IN, _only_ the patched
signal reaches the filter. This allows the adaptor's mixer to fully control
the signal levels.

This mod is officially documented, but in a document which is, for some reason,
no longer linked from Moog's official Werkstatt-01 manuals page:

https://api.moogmusic.com/sites/default/files/2018-04/Werkstatt_Expansion_Board_Final.pdf

(Page 2, bottom right-hand corner.)

## Why?

Because I'm the kind of nerd who enjoys open source, making music, and making
things to make music with.

# Copyright

werkstatt-adaptor © 2024 by Philip Allison is licensed under CC BY-NC-SA 4.0
