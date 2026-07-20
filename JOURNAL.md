## July 20th: Setting everything up and doing schematic, also BOM.
Alright I finished setting up the repo, now i"m gonna find parts for the BOM from LCSC. We will be using the Seeed XIAO ESP32-C3 because its tiny and it has bulit in battery charging and I"m quite experienced with it before
While I was designing the schematic, I feel like there should probably a button to turn on the game console otherwise it'll just be draining power. I also added an OLED as how else would you be able to see the game? I used net labels for the SCL and SDA that are shared between the OLED and the accelerometer For the accelerometer for the PCB, we need a capacitor of 220 nF, a capacitor of 10 uF, a capacitor of 100 nF, and finally a capacitor of 100nF. Current BOM:
1 Seeed XIAO ESP32-C3 | https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started/
1 LiPo Battery
1 0.96 " OLED | https://www.lcsc.com/product-detail/C5248080.html
1 Tactile Button | https://www.lcsc.com/product-detail/C2913653.html
1 Accelerometer | https://www.lcsc.com/product-detail/C2913653.html
1 Capacitor Of 220 nF | https://www.lcsc.com/product-detail/C412252.html
2 Ceramic Capacitors Of 100 nF | https://www.lcsc.com/product-detail/C60474.html
1 Aluminum Capacitor of 10 uF | https://www.lcsc.com/product-detail/C192100.html
1 Buzzer | https://www.lcsc.com/product-detail/C49246964.html


I've found all the parts and I've imported them to KICAD, now I just need to wire them and stuff!
I've decided to add a buzzer for sound of the game!. I finally finished wiring up the accelerometer, it had a lot of things that I needed to read the PDF for. Because I'm using I2C because my MCU is the Seeed XIAO ESP32-C3. I needed to wire the CS of the accelerometer to the VDD_IO. ![image](https://cdn.hackclub.com/019f81e7-0af2-7f93-a6bb-4fbecc54df9e/paste-1784590829923.png). Everything else to wire was relatively simple as they had a very nice diagram! ![image](https://cdn.hackclub.com/019f81e7-9217-73f3-a406-ef5207f4ab1e/paste-1784590864319.png)

I also have to remember that I need to program/configure the INT signals of the accelerometer over I2C using the MCU. Otherwise they won't do anything. I finished the schematic!
![image](https://cdn.hackclub.com/019f81f1-bb86-72b7-afe0-1921dfae7bf1/paste-1784591530324.png)

I'll do the PCB tomorrow and update the README with the BOM along with proper costs!

### Lapse Link: 