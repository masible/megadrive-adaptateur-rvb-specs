# megadrive-adaptateur-rvb-specs
Technical information about the RGB adapter ("Adaptateur R.V.B.") shipped
with French Mega Drives.

## External documentation

- [Using the RVB adapter for NTSC output (French)](http://www.segakore.fr/index.php/2004/08/07/mega-drive-modifiez-votre-cable-rgb-fr-vers-pal-ntsc)
- [Sega RGB cable](https://segaretro.org/Sega_Master_System#Sega_RGB_Cable)

## Board

![PCB](images/adaptateur-rvb.jpg)

## Capacitors replacement

Capacitor | Values | Form factor
------------ | ------------- | -------------
C1 | 220 µF 25V | radial
C2 | 100 µF 10V | radial
C5 | 220 µF 25V | radial
C6 | 10 µF 16V | radial

![PCB](images/adaptateur-rvb-layer.jpg)

## Inductor replacement

As you can see in the above picture, L1 (a 3.7Ω 0.27mH inductor) is
missing. The TL497ACN chip in its `BASIC CONFIGURATION
(Peak Switching Current = I(PK) < 500 mA)` ([page 5 of the datasheet](https://www.ti.com/lit/ds/symlink/tl497a.pdf))
is the only configuration using a coil between pins 13 and 10 of this
voltage regulator, but seems to work correctly without it. Caveat emptor.

## License

See [license file](LICENSE)
