
### Pre

* [GPIO](http://en.wikipedia.org/wiki/General%20Purpose%20Input/Output)
* [GPIO access conventions on Linux](http://www.mjmwired.net/kernel/Documentation/gpio.txt)
* [mmc_over_gpio](http://wiki.openwrt.org/doc/howto/mmc_over_gpio)
* [GPIOs of AR913x SoC](http://wiki.openwrt.org/toh/tp-link/tl-wr1043nd#gpios)
* [oldwiki GPIO](http://wiki.openwrt.org/oldwiki/port.gpio)

### Hardware

GPIOs are commonly used in router devices for buttons or leds. They only safely supply or sink (pull to GND) a maximum of 4mA aprox., and the voltage is usually 3V when active. Only two states are posible: high or low. Depending on how a device is activated by a GPIO, active low or active high is defined.

* **active high**: the device is activated when the GPIO is HIGH.

* **active low**: the device is activated when the GPIO is LOW.

In this image you can see how a GPIO is wired to buttons or leds, to work as active low or high.

GPIOs can be also used for complex tasks: 
       |    kernel module   | description
-------|--------------------|-------------
1-wire | kmod-w1-master-gpio| 1-wire bus master
PWN    | kmod-pwm-gpio      | pulse width modulator
SPI    | kmod-spi-gpio      | bitbanging Serial Peripheral Interface
       | kmod-mmc-over-gpio | [MMC/SD card over GPIO](http://wiki.openwrt.org/doc/howto/mmc_over_gpio)
 I2C   | kmod-i2c-gpio      | bitbanging I2C

### Refs

* <http://wiki.openwrt.org/doc/hardware/port.gpio>
