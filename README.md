# M922 · Filters

Ward-Beck Systems M922, 1994|27. Wiki page: [M922 on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M922.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 9 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 12 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 2 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 3 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 6 |
| [SOFTWARE/](SOFTWARE/) | program listings, firmware, the plugin | 1 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 2 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 19 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

**On the WBSps forum (2006|39 - 2014|47):** [1 topic](FORUM.md): what owners and technicians said about it.

## Specifications

From the technical data sheet: [1995 - M922 - DOC - 14-152-02-003 - COMPONENT LAYOUT.wp](MANUALS/1995%20-%20M922%20-%20DOC%20-%2014-152-02-003%20-%20COMPONENT%20LAYOUT.wp) page 1 (read by OCR; check against the page). As data: [`Specifications.json`](Specifications.json).

| | |
|---|---|
| **Gain** | Unity, ±0.5 dB. |
| **Frequency response** | ±0.5 dB from 20 Hz to 20 kHz with the equalizer inserted, high pass filter disabled, and the cut and boost controls in their centre detent position. |
| **Noise** | -90 dBm absolute (20 Hz to 20 kHz), equalizer cut/boost controls in their centre detent position. |
| **Total harmonic distortion** | Less than 0.25% from 20 Hz to 20 kHz at +20 dBu output or less. Less than 0.01% at 1 kHz at +20 dBu output level. |
| **Source impedance** | 300 ohms or less, unbalanced. 600 ohms or less, balanced. |
| **Input impedance** | Greater than 10K ohms unbalanced; 20K ohms balanced. |
| **Input level** | -6 dBu nominal, +20 dBu maximum. |
| **Output impedance** | 30 ohms or less unbalanced. |
| **Load impedance** | 5K ohms or greater. |
| **Output level** | -6 dBu nominal, +21 dBu maximum. |
| **Channel separation** | Greater than -80 dB 20 Hz to 20 kHz. |
| **Phasing** | Input and Output are in phase with the equalizing controls in the centre detent position. |
| **Equalization tracking** | Within 1 dB. |
| **Power requirements** | ±23 volts DC (M922 120 mA), (M922A 65 mA). |
| **Ambient temperature** | 0 to 50 degrees Celsius. |
| **Dimensions** | 1.5&quot; wide x 8&quot; high x 6.6&quot; deep. (38mm x 203mm x 168mm). |
| **Weight** | M922 14 ounces, (400 grams). M922A 14 ounces, (400 grams). GENERAL M922/M922A EQUALIZER MODULES The M922/M922A Stereo and Mono Equalizers operate in conjunction with the M901 series of input modules. A High-Pass filter with a 75 Hz corner frequency maybe inserted separately, pre-equalizer, or not at all. Insertion is tallied by the LED located in the insertion switch. The equalizer separates the audio into three separate bands. Low frequencies from 20 Hz to 500 Hz are adjustable over ±15 dB of range. The low frequency section imparts a shelving response to the audio spectrum. High frequencies are also equalized with a shelving characteristic. Continuously adjustable boost or cut (+15 dB) is provided. The high frequency section can tailor the signal response from 1.8 kHz to 15 kHz. The mid frequency section controls equalization of signal from 400 Hz to 6.4 kHz, and has a bell-shaped characteristic curve. This section has a ±15 dB adjustment range. The quality factor (&quot;Q&quot;) is 2. The equalizer insertion switch is provided with an integral LED totally it's operation. All insertion switching in the M922/M922A is performed using solid-state analog switches. No audio is switched directly from the front panel. The equalizer is packaged ina single module size of 1.5&quot; wide x 8.0&quot; high x 6.6&quot; deep. The M922/M922A is powered by ±23 volts DC. |

## Circuit description

From [1995 - M922 - DOC - 14-152BC - PARTS LIST.wp](MANUALS/1995%20-%20M922%20-%20DOC%20-%2014-152BC%20-%20PARTS%20LIST.wp) page 1 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

**SA14-152B/SA14-152C FILTER ASSEMBLIES**

This circuit description will apply to the left channel of the SA14-152B only. The SA14-152C utilizes only the left channel circuitry.

Low Frequency Low Pass Filter

The low frequency shelving network is comprised of R30, C29, C30 and variable frequency control R4 (part of the M922).

Buffer amplifier U6 isolates the frequency determining components from the equalizer summing amplifier.

Mid Frequency State Variable Filter

The mid-frequency state variable filter consists of an inverting buffer amplifier (U1A), a combining amplifier (U1B) and two low pass filters (­integrators made up of U2A, U2B, C6, C10). The external frequency control; R5, is located on the M922.

The filter input is asserted at P1-1. The filter output appears at P1-2. High Frequency High Pass Filter

Amplifier U5A buffers the high pass filter network from the external cut/boost control.

Capacitor C26, C27 and resistors R28 &amp; R6 (on the M922) determine the corner frequency of the high pass filter. Buffer U6B isolates the frequency determining components from the summing amplifier U3D on the M922. C1 Capacitor 4.7 uF/10 V ITT 4.7M10 C2 &quot; 100 pF Philips 638-58101 C3 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C4 &quot; 4.7 uF/10 V ITT 4.7M10 C5 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN

C6 &quot; 8200 pF &quot; 2222-809-05003 C7 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C8 &quot; 10 uF/25 V ITT 10M25 C9 &quot; 100 pF Philips 638-58101 C10 &quot; 8200 pF Sprague 2222-809-05003

C11 &quot; 0.1 uF/100 V &quot; K104K20X7RFVBWN C12 to C22 delete C23 &quot; 1 uF/35 V ITT 1M35 C24 &quot; 100 pF Philips 638-58101 C25 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN

C26 &quot; 330 pF Philips 638-03331 C27 &quot; 3900 pF Aselco CQ92-MC-100-392M C28 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C29 &quot; 0.022 pF Aselco CQ92-MC-100-223M C30 &quot; 0.047 pF &quot; CQ92-MC-100-473M

C31 &quot; 10 uF/25 V ITT 10M25 C32 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C33 &quot; 0.1 uF/100 V &quot; &quot; C34 &quot; 10 uF/25 V ITT 10M25 C35 &quot; 10 uF/25 V &quot; &quot;

C36 * &quot; 4.7 uF/10 V ITT 4.7M10 C37 &quot; 100 pF Philips 638-58101 C38 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C39 &quot; 4.7 uF/10 V ITT 4.7M10 C40 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN

C41 &quot; 8200 pF &quot; 2222-809-05003 C42 &quot; 0.1 uF/100 V &quot; K104K20X7RFVBWN C43 &quot; 10 uF/25 V ITT 10M25 C44 &quot; 100 pF Philips 638-58101 C45 &quot; 8200 pF Sprague 2222-809-05003

C46 &quot; 0.1 uF/100 V &quot; K104K20X7RFVBWN C47 to C57 delete C58 &quot; 1 uF/35 V ITT 1M35 C59 &quot; 100 pF Philips 638-58101 C60 Capacitor 0.1 uF/100 V Sprague K104K20X7RFVBWN C61 &quot; 330 pF Philips 638-03331 C62 &quot; 3900 pF Aselco CQ92-MC-100-392M C63 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C64 &quot; 0.022 pF Aselco CQ92-MC-100-223M

C65 &quot; 0.047 pF &quot; CQ92-MC-100-473M C66 &quot; 10 uF/25 V ITT 10M25 C67 &quot; 0.1 uF/100 V Sprague K104K20X7RFVBWN C68 &quot; 0.1 uF/100 V &quot; &quot;

P1 Connector 20 Pin Bergstik Berg 65645-120

P3 &quot; 6 Pin Bergstik &quot; 65645-106

R1 Resistor 1/4W 5% 100 Philips CR25

**R12 &quot; &quot; 3K &quot; &quot;**

R13 to R24 delete R25 Resistor 1/4W 5% 100 Philips CR25

**R36 &quot; &quot; 15K &quot; &quot;**

R37 Resistor 1/4W 5% 15K Philips CR25

**R43 &quot; &quot; 3K &quot; &quot;**

R44 to R55 delete R56 Resistor 1/4W 5% 100 Philips CR25

**R62 &quot; &quot; 1K &quot; &quot;**

U1 Integrated Circuit National LM833N

U3, U4 delete U5 Integrated Circuit National LM833N

U9, U10 delete U11 Integrated Circuit National LM833N

* Note: C36 to C68 deleted from SA14-152C R32 to R62 U7 to U12

</details>

<!-- /module data -->

## Photos

_Photographs of the module itself: front, back, inside, racked._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKeERaWXhzcW1xZlU/view?resourcekey=0-tPJ3YmlasEwu6bbHn0-_QA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKeERaWXhzcW1xZlU&resourcekey=0-tPJ3YmlasEwu6bbHn0-_QA" width="240" alt="1994 - M922 - 3c47_3.jpg"></a><br><sub>1994|27 · 3c47_3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKN3g4NDQ0cm8zMUk/view?resourcekey=0-R81Tpow6A4Xds86iGlZAOg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKN3g4NDQ0cm8zMUk&resourcekey=0-R81Tpow6A4Xds86iGlZAOg" width="240" alt="1994 - M922 - 4466_3.jpg"></a><br><sub>1994|27 · 4466_3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKYi1aOVBYTlBRWE0/view?resourcekey=0-b0bU4bHoHRrVsjCkOyEJBQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKYi1aOVBYTlBRWE0&resourcekey=0-b0bU4bHoHRrVsjCkOyEJBQ" width="240" alt="1994 - M922 - 45bd_3.jpg"></a><br><sub>1994|27 · 45bd_3</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZmtsVEkyZDE4Tlk/view?resourcekey=0-LQ-EurHyreHewffTFOujdw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZmtsVEkyZDE4Tlk&resourcekey=0-LQ-EurHyreHewffTFOujdw" width="240" alt="1994 - M922 - 47bd_3.jpg"></a><br><sub>1994|27 · 47bd_3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbWkwM0c4bFFPeDA/view?resourcekey=0-9ZwnAcr0p2zQ31Cr6FelHA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbWkwM0c4bFFPeDA&resourcekey=0-9ZwnAcr0p2zQ31Cr6FelHA" width="240" alt="1994 - M922 - M 922 &amp; M 901 C...Channel Strip (1) ea_.jpg"></a><br><sub>1994|27 · M 922 &amp; M 901 C...Channel Strip (1) ea_</sub></td></tr>
</table>

## Mechanical

_Mechanical drawings: front panels, cover plates, metalwork and hardware (-03- drawings), AutoCAD files, each with its `(EXTRACTED).svg` vectors; `<module> - front panel.svg` is the front panel as vectors._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/18hZ0lifdNQp8IvJRBvDuT1FEzig8uTDJ/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=18hZ0lifdNQp8IvJRBvDuT1FEzig8uTDJ" width="240" alt="19xx - M922 - DOC - 922-03-001 - SEE DETAIL NOTE ORIENTATIONS REQ'D FAR SIDE.jpg"></a><br><sub>19xx - M922 - DOC - 922-03-001 - SEE DETAIL NOTE ORIENTATIONS REQ'D FAR SIDE</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1kuC5LOv6aGX37O75sEjJnDpnN2D01llf/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1kuC5LOv6aGX37O75sEjJnDpnN2D01llf" width="240" alt="19xx - M922 - DOC - 922-03-001 - STEREO EQUALIZER MODULE.png"></a><br><sub>19xx - M922 - DOC - 922-03-001 - STEREO EQUALIZER MODULE</sub></td></tr>
</table>

Not on Google Drive yet: `19xx - 922-03-001 - M922A STEREO EQUALIZER MODULE - DRN DRG - ISS 3.jpg`

## 3-D model

[`MECHANICAL/M922.stl`](MECHANICAL/M922.stl) (GitHub turns it in 3-D) · [view, change and generate it on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/2026/stl.html?m=M922)

- **Size:** 38 × 203 mm panel, 168 mm deep, 3.2 mm plate (TECHNICAL DATA: 1.5" wide x 8" high x 6.6" deep. (38mm x 203mm x 168mm).)
- **From the drawing:** 6 holes and cut-outs, 0 knobs (front panel: `MECHANICAL/M922 - front panel.svg`)
- Made by `tools/module_models.py` (→ `MECHANICAL/M922.model.json`) and `tools/stl/make_stl.mjs` in [WBSps.ca](https://github.com/WardBeckSystems/WBSps.ca); the site makes the same STL from the same JSON.

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [M922.kicad_sym](KICAD/M922.kicad_sym)
- [index.html](KICAD/index.html)

## Software

- [index.html](SOFTWARE/index.html)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
