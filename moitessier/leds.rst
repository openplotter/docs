Status LEDs
###########

.. image:: img/leds1.png

.. image:: img/leds2.png

Error Output

The ERRORLED indicates the following error types:•Minor/temporary  error:  Every  NMEA  source  (AIS,  GNSS)  and  every  NMEA  output (SPI  interface  to  Raspberry  Pi)  is  assigned  a  memory  areain  the  microcontrollerin the form of a buffer. The data of multiple inputs iswritten to the SPI buffer. If data is written to this buffer quicker than it is read by the Raspberry Pi, the buffer will be full after a certain time due to its memory restrictions. In such a case,no more data can be  written  and abuffer  overflowoccurs.As  soon  as  the  buffer  is  read,  the  device continuous to process data.•Serious(system)errors: The device is running a self-test after each reset. If an error occursduring  hardware initialization,the ERRORLED flashes  in  a  constant pattern. The  device  can  no  longer  be  used  in  this  case.  If  a  restart  does  not  resolve  the problem, please contact the Rooco support team.You can read the system errors by reading the device information.pi> ~/moitessier/app/moitessier_ctrl/moitessier_ctrl /dev/moitessier.ctrl 1The error is coded as bit pattern:•Bit 0: GNSS failed•Bit 1: AIS receiver 1 failed•Bit 2: AIS receiver 2 failed•Bit 3: SPI host interface failed•Bit 4: UART host interface failede.g. system errors = 0x00000011→GNSS and UART host interface failed