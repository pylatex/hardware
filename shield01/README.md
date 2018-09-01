# SH01: Placa de Sensores Varios

Esta placa permite integrar y verificar la funcionalidad de varios sensores disponibles en el Grupo GITUD

## Pruebas de Funcionamiento:

1. Verificacion de Etapa de Potencia
   
   En el pin 7 de J1 debe haber un voltaje cercano a 3.3V. En otro caso, revisar el valor de R2. Se recomienda tener conectada una batería de Litio en el conector SYSBAT.

2. GPS
   
   Batería CR2032 en el portapilas GPSBATT, necesaria para que el GPS mantenga la hora en caso que se desenergize el sistema. Una vez conectada, y con alimentacion disponible (sea por USB y/o batería de Litio), conectar un depurador serial a los pines 4 (GNS_TX) y 18 (GNS_RX), configuracion 9600 8N1. Con un cliente de terminal acceder al depurador serial, cada segundo se debe recibir un paquete de sentencias NMEA. Por defecto se encuentra habilitado, para apagarlo es necesario aplicar un 0 en el pin 11 (GNS_SHUTDOWN).

3. Dispositivos I2C
   
   Uno de ellos se energiza de la Etapa de Potencia del paso 1, directamente. El pin 12 (IAQ_SHUTDOWN) sirve para apagar el sensor de CO2 iAQ Core C, al el estado por defecto es habilitado.

   Dado que los otros dispositivos I2C de la placa consumen poca energía, se pueden energizar directamente de un pin del microcontrolador, colocando 3.3V en el pin 2 (VCC_SENS). Para pruebas externas, si se probó la etapa de potencia, basta con puentearlo a la salida de 3.3V (pin 7).