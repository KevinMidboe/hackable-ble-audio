# hackable-ble-audio
Project to research, find and create a hackable platform for smart audio connectivity and seamless transmission between receiving and transmitting devices on same channel


## Idea
Keypoints: 
looked at what my ble trans/receiver I had in its guts in, [images here](./resources/aukey%20board%20images). 
The main chips I see are:
 - csr8670 - Bluetooth Audio SoC [more info](#csr8670)
 - sgm3717 - 4Ω, 400MHz Bandwidth, Dual, SPDT Negative Signal Handling Analog Switch [more info](#sgm3717)
 - p8908 - 25mW TRUE CAP FREE STEREO HEADPHONE AMPLIFIER [more info](#p8908) 



# csr8670

The csr8670 is a SoC with BLE, embedded flash for receiving and outputing audio signals.


Important note is that the csr8670 in my device has a newer version, the 8675.  
In a product newsletter from Shenzhen Feasycom has a overviewed comparison between the old and new models [0].

csr8670 | csr8675 | notes
-- | -- | --
BT4.0 | BT4.1 | OS upgrade to BT 5.0
80 Mhz RISC MCU and 80 MIPS Kalimba DSP
16-bit audio | 24-bit audio | 
8-96kHz | 8-192kHz | Supported sample rates
16Mb Flash | 16Mb Flash | External 64Mb SPI Flash
Stereo codec and 2 path MIC | Stereo codec and 2 path MIC |
1 x I²S/PCM | 2 x I²S/PCM | Meet the needs of multiple digital audio interfaces
SPDIF (blocks  I²S/PCM's) | SPDIF (non-blocking I²S/PCM)
UART, USB2.0 full-speed, I²C | UART, USB2.0 full-speed, I²C & SPI | Serial interfaces
 | Master and slave bit-serialiser (I²C and  SPI) | 
6 capacitive touch sensor inputs
Battery charger
3 LED and LCD segment driver
29 PIO ports | 32 PIO ports | Up to w/ BGA package


## Documetation & references
 - Product Page [qualcomm.com](https://www.qualcomm.com/products/csr8670) [pdf](./resources/csr8670/CSR8670%20%7C%20Qualcomm%20Productbrief.pdf)
 - Product Brief [qualcomm.com](https://www.qualcomm.com/media/documents/files/csr8670-product-brief.pdf) [pdf](./resources/csr8670/CSR8670%20%7C%20Qualcomm%20Productpage.pdf)
 - Digikey product page [digikey](https://www.digikey.com/catalog/en/partgroup/csr8670/28987) [pdf](./resources/csr8670/CSR8670%20-%20Qualcomm%20-%20Integrated%20Circuits%20%28ICs%29%20%7C%20Online%20Catalog%20%7C%20DigiKey%20Electronics.pdf)
 - [0] CSR8670 vs CSR8675 [feasy.com](http://www.feasycom.net/news/difference-between-csr8670-and-csr-15721421.html) [pdf](./resources/csr8670/CSR8670%20vs%20CSR8675%20-%20Product%20News%20-%20Shenzhen%20Feasycom%20Technology%20Co.%2CLtd%20%7C%20feasycom.net)


## Sources

TODO: 
Chip maker, info and important takeaways.  
Pros and cons.  


