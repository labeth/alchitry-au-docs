# alchitry-au-docs
This is repository to collect info about the alchitry au fpga
https://alchitry.com/collections/all/products/alchitry-au-fpga-development-board
# Function Descriptions
## Raw +5V
Raw +5V input from the usb
## Differential IO
Differential signaling is a method for electrically transmitting information using two complementary signals.
https://en.wikipedia.org/wiki/Differential_signaling
## Single Ended IO
Single-ended signaling is the simplest and most commonly used method of transmitting electrical signals over wires. One wire carries a varying voltage that represents the signal, while the other wire is connected to a reference voltage, usually ground.
https://en.wikipedia.org/wiki/Single-ended_signaling
## Dual Voltage IO
Voltage level can be changed between 1.8V and 3.3V using the VBSEL pin
## Analog Input
An analog signal is any continuous signal for which the time-varying feature (variable) of the signal is a representation of some other time varying quantity, i.e., analogous to another time varying signal. For example, in an analog audio signal, the instantaneous voltage of the signal varies continuously with the pressure of the sound waves. It differs from a digital signal, in which the continuous quantity is a representation of a sequence of discrete values which can only take on one of a finite number of values.
https://en.wikipedia.org/wiki/Analog_signal
## LED*
A light-emitting diode (LED) is a semiconductor light source that emits light when current flows through it. There are 8 LEDs connected to the board named 0-7
https://en.wikipedia.org/wiki/Light-emitting_diode
## VBSEL
Controls dual voltage IO levels  Leave floating for 3.3V IO  Connect to 1.8V for 1.8V IO
## USB_TX
This is the transmit side of the Universal Serial Bus (USB). USB is an industry standard that establishes specifications for cables and connectors and protocols for connection, communication and power supply (interfacing) between computers, peripherals and other computers.
https://en.wikipedia.org/wiki/USB
## USB_RX
This is the recive side of the Universal Serial Bus (USB). USB is an industry standard that establishes specifications for cables and connectors and protocols for connection, communication and power supply (interfacing) between computers, peripherals and other computers.
https://en.wikipedia.org/wiki/USB
## TDI
Test Data In pin of the JTAG interface. JTAG (named after the Joint Test Action Group which codified it) is an industry standard for verifying designs and testing printed circuit boards after manufacture.
https://en.wikipedia.org/wiki/JTAG
## TDO
Test Data Out pin of the JTAG interface. JTAG (named after the Joint Test Action Group which codified it) is an industry standard for verifying designs and testing printed circuit boards after manufacture.
https://en.wikipedia.org/wiki/JTAG
## TCK
Test Clock pin of the JTAG interface. JTAG (named after the Joint Test Action Group which codified it) is an industry standard for verifying designs and testing printed circuit boards after manufacture.
https://en.wikipedia.org/wiki/JTAG
## TMS
Test Mode Select pin of the JTAG interface. JTAG (named after the Joint Test Action Group which codified it) is an industry standard for verifying designs and testing printed circuit boards after manufacture.
https://en.wikipedia.org/wiki/JTAG
## Program
If you need some external device to reset the FPGA, the PROGRAM_B_0 pin is the means by which this is accomplished.  PROGRAM_B_0 pulled LOW will provoke a 'cold boot', the FPGA will re-load its configuration (program).  Using the PROGRAM_B_0 pin is the simpler alternative to cycling power to the FPGA.
## Done
A High signal on the DONE pin indicates completion of the configuration sequence. The DONE output is an open-drain output by default.
Note: DONE has an internal pull-up resistor of approximately 10kΩ. There is no setup/hold requirement for the DONE register. These changes, along with the DonePipe register software default, eliminate the need for the DriveDONE driver-option. External 330Ω resistor circuits are not required but can be used as they have been in previous generations.
## Reset
Has a button named reset, should normaly be configured to reset the device on push by developer.
## 100MHz Clock
The clock input into the FPGA, you can use a PLL to get other speeds based on this clock
https://hardwarebee.com/ultimate-guide-fpga-clock/


# Bank A

|Port   |Schematic |Name                           |Function1        |Function2         |
|---    |---       |---                            |---              |---               |
|A1     | +5V      | None: marked (R) on Br board  | Raw +5V         |                  |
|A2     | T8/1.2D  | IO_L21N_T3_DQS_A06_D22_14     | Differential IO |                  |
|A3     | T7/1.2D  | IO_L21P_T3_DQS_14             | Differential IO |                  |
|A4     | GND      | None: marked (G) on Br board  |                 |                  |
|A5     | T5/1.2D  | IO_L23N_T3_A02_D18_14         | Differential IO |                  |
|A6     | R5/1.2D  | IO_L23P_T3_A03_D19_14         | Differential IO |                  |
|A7     | +3V3     | None: marked (+V) on Br board |                 |                  |
|A8     | R8/1.2D  | IO_L20N_T3_A07_D23_14         | Differential IO |                  |
|A9     | P8/1.2D  | IO_L20P_T3_A08_D24_14         | Differential IO |                  |
|A10    | GND      | None: marked (G) on Br board  |                 |                  |
|A11    | L2/1.4D  | O_L23N_T3_35                  | Differential IO |                  |
|A12    | L3/1.4D  | IO_L23P_T3_35                 | Differential IO |                  |
|A13    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A14    | J1/1.4D  | IO_L22N_T3_35                 | Differential IO |                  |
|A15    | K1/1.4D  | IO_L22P_T3_35                 | Differential IO |                  |
|A16    | GND      | None: marked (G) on Br board  |                 |                  |
|A17    | H1/1.4D  | IO_L20N_T3_35                 | Differential IO |                  |
|A18    | H2/1.4D  | IO_L20P_T3_35                 | Differential IO |                  |
|A19    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A20    | G1/1.4C  | IO_L17N_T2_35                 | Differential IO | Single Ended IO  |
|A21    | G2/1.4C  | IO_L17P_T2_35                 | Differential IO | Single Ended IO  |
|A22    | GND      | None: marked (G) on Br board  |                 |                  |
|A23    | K5/1.4D  | IO_25_35                      | Single Ended IO |                  |
|A24    | E6/1.4A  | IO_0_35                       | Single Ended IO |                  |
|A25    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A26    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A27    | M6/1.2D  | IO_L19P_T3_A10_D26_14         | Differential IO | Single Ended IO  |
|A28    | N6/1.2D  | IO_L19N_T3_A09_D25_VREF_14    | Differential IO | Single Ended IO  |
|A29    | GND      | None: marked (G) on Br board  |                 |                  |
|A30    | H5/1.4D  | IO_L18P_T2_35                 | Differential IO | Single Ended IO  |
|A31    | H4/1.4D  | IO_L18N_T2_35                 | Differential IO | Single Ended IO  |
|A32    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A33    | J3/1.4D  | IO_L21P_T3_DQS_35             | Differential IO |                  |
|A34    | H3/1.4D  | IO_L21N_T3_DQS_35             | Differential IO |                  |
|A35    | GND      | None: marked (G) on Br board  |                 |                  |
|A36    | J5/1.4D  | IO_L19P_T3_35                 | Differential IO |                  |
|A37    | J4/1.4D  | IO_L19N_T3_VREF_35            | Differential IO |                  |
|A38    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A39    | K3/1.4D  | IO_L24P_T3_35                 | Differential IO |                  |
|A40    | K2/1.4D  | IO_L24N_T3_35                 | Differential IO |                  |
|A41    | GND      | None: marked (G) on Br board  |                 |                  |
|A42    | N9/1.2D  | IO_L18P_T2_A12_D28_14         | Differential IO |                  |
|A43    | P9/1.2D  | IO_L18N_T2_A11_D27_14         | Differential IO |                  |
|A44    | +3V3     | None: marked (+V) on Br board |                 |                  |
|A45    | R7/1.2D  | IO_L24N_T3_A00_D16_14         | Differential IO |                  |
|A46    | R6/1.2D  | IO_L24P_T3_A01_D17_14         | Differential IO |                  |
|A47    | GND      | None: marked (G) on Br board  |                 |                  |
|A48    | T9/1.2D  | IO_L22P_T3_A05_D21_14         | Differential IO |                  |
|A49    | T10/1.2D | IO_L22N_T3_A04_D20_14         | Differential IO |                  |
|A50    | +5V      | None: marked (+V) on Br board |                 |                  |

# Bank B

|Port   |Schematic |Name                           |Function1        |Function2         |Function 3    |
|---    |---       |---                            |---              |---               |---           |
|B1     | +5V      | None: marked (R) on Br board  | Raw +5V         |                  |              |
|B2     | D1/1.4C  | IO_L10N_T1_AD15N_35           | Single Ended IO | Differential IO  | Analog Input |
|B3     | E2/1.4C  | IO_L10P_T1_AD15P_35           | Single Ended IO | Differential IO  | Analog Input |
|B4     | GND      | None: marked (G) on Br board  |                 |                  |              |
|B5     | A2/1.4B  | IO_L8N_T1_AD14N_35            | Single Ended IO | Differential IO  | Analog Input |
|B6     | B2/1.4B  | IO_L8P_T1_AD14P_35            | Single Ended IO | Differential IO  | Analog Input |
|B7     | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B8     | E1/1.4C  | IO_L15N_T2_DQS_35             | Single Ended IO | Differential IO  |              |
|B9     | F2/1.4C  | IO_L15P_T2_DQS_35             | Single Ended IO | Differential IO  |              |
|B10    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B11    | F3/1.4C  | IO_L14N_T2_SRCC_35            | Single Ended IO | Differential IO  |              |
|B12    | F4/1.4C  | IO_L14P_T2_SRCC_35            | Single Ended IO | Differential IO  |              |
|B13    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B14    | A3/1.4B  | IO_L4N_T0_35                  | Single Ended IO | Differential IO  |              |
|B15    | B4/1.4B  | IO_L4P_T0_35                  | Single Ended IO | Differential IO  |              |
|B16    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B17    | A4/1.4B  | IO_L3N_T0_DQS_AD5N_35         | Single Ended IO | Differential IO  | Analog Input |
|B18    | A5/1.4B  | IO_L3P_T0_DQS_AD5P_35         | Single Ended IO | Differential IO  | Analog Input |
|B19    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B20    | B5/1.4B  | IO_L2N_T0_AD12N_35            | Single Ended IO | Differential IO  | Analog Input |
|B21    | B6/1.4B  | IO_L2P_T0_AD12P_35            | Single Ended IO | Differential IO  | Analog Input |
|B22    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B23    | A7/1.4B  | IO_L1N_T0_AD4N_35             | Single Ended IO | Differential IO  | Analog Input |
|B24    | B7/1.4A  | IO_L1P_T0_AD4P_35             | Single Ended IO | Differential IO  | Analog Input |
|B25    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B26    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B27    | C7/1.4B  | IO_L5P_T0_AD13P_35            | Single Ended IO | Differential IO  | Analog Input |
|B28    | C6/1.4B  | IO_L5N_T0_AD13N_35            | Single Ended IO | Differential IO  | Analog Input |
|B29    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B30    | D6/1.4B  | IO_L6P_T0_35                  | Single Ended IO | Differential IO  |              |
|B31    | D5/1.4B  | IO_L6N_T0_VREF_35             | Single Ended IO | Differential IO  |              |
|B32    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B33    | F5/1.4C  | IO_L13P_T2_MRCC_35            | Single Ended IO | Differential IO  |              |
|B34    | E5/1.4C  | IO_L13N_T2_MRCC_35            | Single Ended IO | Differential IO  |              |
|B35    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B36    | G5/1.4C  | IO_L16P_T2_35                 | Single Ended IO | Differential IO  |              |
|B37    | G4/1.4C  | IO_L16N_T2_35                 | Single Ended IO | Differential IO  |              |
|B38    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B39    | D4/1.4C  | IO_L12P_T1_MRCC_35            | Single Ended IO | Differential IO  |              |
|B40    | C4/1.4C  | IO_L12N_T1_MRCC_35            | Single Ended IO | Differential IO  |              |
|B41    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B42    | E3/1.4C  | IO_L11P_T1_SRCC_35            | Single Ended IO | Differential IO  |              |
|B43    | D3/1.4C  | IO_L11N_T1_SRCC_35            | Single Ended IO | Differential IO  |              |
|B44    | +3V3     | None: marked (+V) on Br board |                 |                  |              |
|B45    | C3/1.4B  | IO_L7P_T1_AD6P_35             | Single Ended IO | Differential IO  | Analog Input |
|B46    | C2/1.4B  | IO_L7N_T1_AD6N_35             | Single Ended IO | Differential IO  | Analog Input |
|B47    | GND      | None: marked (G) on Br board  |                 |                  |              |
|B48    | C1/1.4B  | IO_L9P_T1_DQS_AD7P_35         | Single Ended IO | Differential IO  | Analog Input |
|B49    | B1/1.4C  | IO_L9N_T1_DQS_AD7N_35         | Single Ended IO | Differential IO  | Analog Input |
|B50    | +5V      | None: marked (+V) on Br board |                 |                  |              |

# Bank C

|Port   |Schematic |Name                           |Function1        |Function2         |Function 3       |
|---    |---       |---                            |---              |---               |---              |
|C1     | +5V      | None: marked (R) on Br board  | Raw +5V         |                  |                 |
|C2     | T13/1.2C | IO_L16N_T2_A15_D31_14         | Single Ended IO | Differential IO  |                 |
|C3     | R13/1.2C | IO_L16P_T2_CSI_B_14           | Single Ended IO | Differential IO  |                 |
|C4     | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C5     | T12/1.2C | IO_L15N_T2_DQS_DOUT_CSO_B_14  | Single Ended IO | Differential IO  |                 |
|C6     | R12/1.2C | IO_L15P_T2_DQS_RDWR_B_14      | Single Ended IO | Differential IO  |                 |
|C7     | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C8     | R11/1.2C | IO_L17N_T2_A13_D29_14         | Single Ended IO | Differential IO  |                 |
|C9     | R10/1.2C | IO_L17P_T2_A14_D30_14         | Single Ended IO | Differential IO  |                 |
|C10    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C11    | N2/1.5B  | IO_L3N_T0_DQS_34              | Single Ended IO | Differential IO  | Dual Voltage IO |
|C12    | N3/1.5B  | IO_L3P_T0_DQS_34              | Dual Voltage IO | Differential IO  |                 |
|C13    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C14    | P3/1.5B  | IO_L5N_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C15    | P4/1.5B  | IO_L5P_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C16    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C17    | M4/1.5A  | IO_L1N_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C18    | L4/1.5A  | IO_L1P_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C19    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C20    | N4/1.5B  | IO_L6N_T0_VREF_34             | Dual Voltage IO | Differential IO  |                 |
|C21    | M5/1.5B  | IO_L6P_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C22    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C23    | L5/1.5A  | IO_0_34                       | Single Ended IO | Dual Voltage IO  |                 |
|C24    | P5/1.5B  | IO_L10P_T1_34                 | Single Ended IO | Dual Voltage IO  |                 |
|C25    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C26    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C27    | T4/1.5B  | IO_L9P_T1_DQS_34              | Dual Voltage IO | Differential IO  |                 |
|C28    | T3/1.5B  | IO_L9N_T1_DQS_34              | Dual Voltage IO | Differential IO  |                 |
|C29    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C30    | R3/1.5B  | IO_L8P_T1_34                  | Dual Voltage IO | Differential IO  |                 |
|C31    | T2/1.5B  | IO_L8N_T1_34                  | Dual Voltage IO | Differential IO  |                 |
|C32    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C33    | R2/1.5B  | IO_L7P_T1_34                  | Dual Voltage IO | Differential IO  |                 |
|C34    | R1/1.5B  | IO_L7N_T1_34                  | Dual Voltage IO | Differential IO  |                 |
|C35    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C36    | N1/1.5B  | IO_L4P_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C37    | P1/1.5B  | IO_L4N_T0_34                  | Dual Voltage IO | Differential IO  |                 |
|C38    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C39    | M2/1.5A  | IO_L2P_T0_34                  | Single Ended IO | Differential IO  | Dual Voltage IO |
|C40    | M1/1.5A  | IO_L2N_T0_34                  | Single Ended IO | Differential IO  | Dual Voltage IO |
|C41    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C42    | N13/1.2C | IO_L11P_T1_SRCC_14            | Single Ended IO | Differential IO  |                 |
|C43    | P13/1.2C | IO_L11N_T1_SRCC_14            | Single Ended IO | Differential IO  |                 |
|C44    | +3V3     | None: marked (+V) on Br board |                 |                  |                 |
|C45    | N11/1.2C | IO_L13P_T2_MRCC_14            | Single Ended IO | Differential IO  |                 |
|C46    | N12/1.2C | IO_L13N_T2_MRCC_14            | Single Ended IO | Differential IO  |                 |
|C47    | GND      | None: marked (G) on Br board  |                 |                  |                 |
|C48    | P10/1.2C | IO_L14P_T2_SRCC_14            | Single Ended IO | Differential IO  |                 |
|C49    | P11/1.2C | IO_L14N_T2_SRCC_14            | Single Ended IO | Differential IO  |                 |
|C50    | +5V      | None: marked (+V) on Br board |                 |                  |                 |

# Bank D

|Port   |Schematic       |Name                            |Function1         |
|---    |---             |---                             |---               |
|D1     | +5V            | None: marked (R) on Br board   | Raw +5V          |
|D2     | LED2/1.5D      | IO_L4P_T0_D04_14               | LED2             |
|D3     | LED3/1.5D      | IO_L5N_T0_D07_14               | LED3             |
|D4     | GND            | None: marked (G) on Br board   |                  |
|D5     | LED6/1.5D      | IO_L6N_T0_D08_VREF_14          | LED6             |
|D6     | LED7/1.5D      | IO_L7N_T1_D10_14               | LED7             |
|D7     | +3V3           | None: marked (+V) on Br board  |                  |
|D8     | R16/1.2C       | IO_L9N_T1_DQS_D13_14           | Differential IO  |
|D9     | R15/1.2B       | IO_L9P_T1_DQS_14               | Differential IO  |
|D10    | GND            | None: marked (G) on Br board   |                  |
|D11    | P14/1.2C       | IO_L12N_T1_MRCC_14             | Single Ended IO  |
|D12    | M15/1.2B       | IO_L3N_T0_DQS_EMCCLK_14        | Single Ended IO  |
|D13    | +3V3           | None: marked (+V) on Br board  |                  |
|D14    | USB_TXD/1.2B   | IO_L8P_T1_D11_14               | USB_TX           |
|D15    | USB_RXD/1.2B   | IO_L8N_T1_D12_14               | USB_RX           |
|D16    | GND            | None: marked (G) on Br board   |                  |
|D17    | A1V8/3.1E      | VCCADC_0: Analog 1.8V          | Analog Supply    |
|D18    | A1V8/3.1E      | VCCADC_0: Analog 1.8V          | Analog Supply    |
|D19    | +3V3           | None: marked (+V) on Br board  |                  |
|D20    | VBSEL/4.5A     | VBSEL: Set Dual Voltage level  | VBSEL            |
|D21    | 1V8/3.4C       | None: +1.8V                    | +1.8V            |
|D22    | GND            | None: marked (G) on Br board   |                  |
|D23    | TDI/5.4B       | TDI_0                          | TDI              |
|D24    | TDO/5.4B       | TDO_0                          | TDO              |
|D25    | +3V3           | None: marked (+V) on Br board  |                  |
|D26    | +3V3           | None: marked (+V) on Br board  |                  |
|D27    | TCK/5.4B       | TCK_0                          | TCK              |
|D28    | TMS/5.4B       | TMS_0                          | TMS              |
|D29    | GND            | None: marked (G) on Br board   |                  |
|D30    | AVN/3.1D       | VN_0                           | Analog Input     |
|D31    | AVP/3.1D       | VP_0                           | Analog Input     |
|D32    | +3V3           | None: marked (+V) on Br board  |                  |
|D33    | AGND/3.2E      | GNDADC_0, VREFN_0              | Analog Supply    |
|D34    | AVREF/3.2D     | VREFP_0                        | Analog Supply    |
|D35    | GND            | None: marked (G) on Br board   |                  |
|D36    | PROGRAM_B/5.6B | PROGRAM_B_0                    | Program          |
|D37    | DONE/5.6B      | DONE_0                         | Done             |
|D38    | +3V3           | None: marked (+V) on Br board  |                  |
|D39    | RESET/1.5D     | IO_25_14                       | Reset            |
|D40    | 100MHZ/1.4E    | IO_L12P_T1_MRCC_14             | 100MHz Clock     |
|D41    | GND            | None: marked (G) on Br board   |                  |
|D42    | T14/1.2C       | IO_L10P_T1_D14_14              | Differential IO  |
|D43    | T15/1.2C       | IO_L10N_T1_D15_14              | Differential IO  |
|D44    | +3V3           | None: marked (+V) on Br board  |                  |
|D45    | LED5/1.5D      | IO_L4N_T0_D05_14               | LED5             |
|D46    | LED4/1.5D      | IO_L7P_T1_D09_14               | LED4             |
|D47    | GND            | None: marked (G) on Br board   |                  |
|D48    | LED1/1.5D      | IO_0_14                        | LED1             |
|D49    | LED0/1.5D      | IO_L5P_T0_D06_14               | LED0             |
|D50    | +5V            | None: marked (+V) on Br board  |                  |

