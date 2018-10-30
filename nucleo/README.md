# Placa Nucleo

Incluye un módulo LoRaWAN [iM880B-L](https://wireless-solutions.de/products/radiomodules/im880b-l.html) y un [PIC16F1769](https://www.microchip.com/wwwproducts/en/PIC16F1769). [Hay un proyecto en GitHub](https://github.com/pylatex/im880b) para controlar el iM88x con comandos HCI desde el PIC.

## Modo Bootloader

Para entrar en modo Bootloader, al momento de emplear el software EndNode Studio
de IMST; *dejar BOOT en alto, y mandar brevemente RESET a tierra.*

| Funcion |  WiMOD  | Nucleo |
|   ----  |   ----  | ----   |
| BOOT    |   26    | 18     | (PULL-DOWN)
| RESET   |    7    | 9      | (PULL-UP)
| VCC     |   17    | 13     |
| GND     |   16    | 19     |
