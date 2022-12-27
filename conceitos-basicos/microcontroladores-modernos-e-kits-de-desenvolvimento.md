---
description: >-
  Alguns exemplos de microcontroladores modernos e placas de desenvolvimento
  acessíveis
---

# Microcontroladores modernos e kits de desenvolvimento

### ATmega328p

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/ATMEGA328P-PU.jpg/1200px-ATMEGA328P-PU.jpg?20121224135142" alt=""><figcaption><p>ATmega328P em sua versão DIP-28N</p></figcaption></figure>

Este microcontrolador é famoso por fazer parte da placa Arduino UNO. É um microcontrolador de 8 bits muito simples, lançado pela finada Atmel e atualmente fabricado pela Microchip. Possui 32 KiB de memória Flash, 2 KiB de memória SRAM e 1 KiB de memória EEPROM. Por ser o microcontrolador do Arduino UNO, pode ser facilmente programado usando o SDK e a IDE do Arduino. Também pode ser programado usando a IDE _Microchip Studio for AVR and SAM devices_.

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Arduino-uno-perspective-transparent.png" alt=""><figcaption><p>Placa Arduino UNO</p></figcaption></figure>

### ESP32

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Espressif_ESP-WROOM-32_Wi-Fi_%26_Bluetooth_Module.jpg" alt=""><figcaption><p>Exemplar de ESP32 soldado em uma placa</p></figcaption></figure>

<figure><img src="https://images.tcdn.com.br/img/img_prod/751846/modulo_esp32_wifi_e_bluetooth_2233_1_20201202141216.jpg" alt=""><figcaption><p>Pequeno módulo ESP-WROOM-32 com antena. Este módulo, bem como outros módulos parecidos, trazem um MCU ESP32 dentro de uma proteção metálica. </p></figcaption></figure>

Esta é, atualmente, uma das famílias de microcontroladores mais populares no meio _maker_. São microcontroladores de 32 bits muito poderosos e de baixo custo. Por possuírem WIFI e Bluetooth embutidos, são perfeitos para projetos IoT. Possuem processadores Xtensa LX6 (single ou dual core), e em versões mais recentes possuem processadores RISC-V.

Para programar os MCUs da família ESP32, a fabricante Espressif disponibiliza um SDK em linguagem C chamado ESP-IDF. No entanto, existem _ports_ do SDK Arduino Core para ESP32, além de algumas bibliotecas baseadas no Arduino Core feitas especialmente para ESP32. Também é possível programar os ESP32 com as linguagens Python e Lua utilizando os firmwares _MicroPython_ e _Lua-RTOS_.

Placas de desenvolvimento com ESP32 são bastante comuns e diversificadas, e muitas delas são _open-hardware_.&#x20;

<figure><img src="https://m.media-amazon.com/images/I/61N65JMQcGL._AC_SL1001_.jpg" alt=""><figcaption><p>Placa de desenvolvimento genérica para ESP32</p></figcaption></figure>

### STM32

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/4/45/STM32H7B0.jpg" alt=""><figcaption><p>Exemplar de STM32 soldado em uma placa</p></figcaption></figure>

STM32 é uma grande família de microcontroladores ARM da fabricante _ST_. Os microcontroladores desta família possuem processadores de 32 bits da família ARM _Cortex-M_ e, em geral, são bem baratos. __ O exemplar mais famoso desta família é o STM32F103C8, com 64KiB de memória flash, 20KiB de memória SRAM e processador _Cortex-M3_.

A forma mais apropriada de programar os STM32 é utilizar as ferramentas STM32CubeMX e STM32CubeIDE, desenvolvidas pela própria _ST_.

* STM32CubeMX é um editor visual de configurações básicas de firmware. Neste software, é possível definir e configurar os recursos do MCU que serão usados e, por fim, gerar uma HAL (_Hardware Abstraction Layer_) em C para o _firmware_.
* STM32CubeIDE é uma IDE própria para programar os STM32, baseada na clássica Eclipse IDE. Com esta IDE, e com um gravador ST-Link, é possível compilar, fazer upload e depurar _firmwares_ desenvolvidos para STM32.

Existem outros meios de programar os STM32, como _ports_ do SDK Arduino _Core_, do sistema operacional MBED e do interpretador MicroPython. No entanto, os MCUs desta família são complexos, e seus recursos só podem ser completamente explorados utilizando as HAL_s_ geradas pelo software STM32CubeMX.

<figure><img src="https://stm32-base.org/assets/img/boards/STM32F103C8T6_Blue_Pill-1.jpg" alt=""><figcaption><p>Placa de desenvolvimento <em>Blue Pill</em>, equipada com um STM32F103C8</p></figcaption></figure>

### RP2040

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/3/35/RP2040_Microcontroller.jpg" alt=""><figcaption><p>RP2040 soldado em uma placa</p></figcaption></figure>

Este microcontrolador é um lançamento de 2021 da _Raspberry Pi Foundation_. Possui dois núcleos ARM _Cortex-M0+_ de 133MHz, 264KiB de memória SRAM e recursos comuns de microcontroladores modernos, como SPI, I2C, UART, DMA, PWM, etc. A princípio, este MCU foi desenvolvido para equipar as placas _Raspberry Pi Pico_, da própria _Raspberry Pi Foundation_, mas com o tempo outras fabricantes passaram a produzir placas com o RP2040.

Como meios de programar o RP2040, a _Raspberry Pi Foundation_ dá duas opções, uma para desenvolvedores profissionais, e outra para iniciantes e hobistas. As opções são, respectivamente, um SDK em C, e um _port_ do interpretador MicroPython.&#x20;

<figure><img src="https://www.filipeflop.com/wp-content/uploads/2021/01/Raspberry-Pi-Pico-1-1.jpg" alt=""><figcaption><p>Placa de desenvolvimento <em>Raspberry Pi Pico</em></p></figcaption></figure>
