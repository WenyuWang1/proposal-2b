# Lab2_Proposal

Work with Xiayu Zeng

## LED
### GIF

![1666326397847979](https://user-images.githubusercontent.com/114005477/197112963-a36c6ebc-540e-452f-873b-63179c8ebd34.gif)

### Code in detail

```
#include <stdio.h>
#include <stdlib.h>
#include "pico/stdlib.h"
#define SDA_PIN 22

int main(){
    stdio_init_all();
    gpio_init(SDA_PIN);
    gpio_set_dir(SDA_PIN, GPIO_OUT);
    while(1){
        gpio_put(SDA_PIN,1);
        sleep_ms(1000);
        gpio_put(SDA_PIN,0);
        sleep_ms(1000);
    }
    return 0;
}
```
## Proposal: Environment Brightness Detection
### Outline:
1. We may focus on the communication between two boards (QT-PY 2040) as well as between the board and APDS-9960.
2. Board A connect to APDS-9960 to detect the environment brightness and tansfer the information to board B.
3. After analyzed the brightness information transferred by board A, board B controls the leds shining frequency and color.
### Why it is cool:
  The information collected by APDS-9960 can also be gesture or distance, thus the boards can transfer the information and control the leds to represent different signals which is quite useful in practical life.
1. We want to use two microcontrollers to design project about communication between microcontrollers (QT-PY 2040), and between microcontroller and APDS-9960.
2. We use the first microcontroller A to connect to APDS-9960 to detect the environment brightness, and use it to send the collected data to microcontroller B.
3. We use microcontroller B to analyze received data of environment brightness, and use microcontroller B to control the color and blinzing frequency of LED.

We think this is cool because we combine several devices we learned before, and we can use them to design something practical. The color detector can be used to identify different color signal to send instructions so as to complete more useful functions.

### Components Requested:
*   Couple wires and resistors.
*   Leds with different colors.
### Questions:
Not now, maybe later.
Current no question, but maybe later.
