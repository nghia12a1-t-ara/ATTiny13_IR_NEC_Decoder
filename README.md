# ATTiny13 IR NEC Decoder

![Hardware Schematic](https://blogger.googleusercontent.com/img/a/AVvXsEgYKno6cLloIPKbAqW4lJKfzND5vSGAoNUs4r4SRekXGHw38I6xwxV2kS6hypeamrFwiC6ug--ub5tGcIb94YuD4KsnraCjE2NqtwV0EnRajN1qB0uwpc72S1W1GWZlOutwlk1LmhKdBoZw4)

## Project Overview

This project demonstrates decoding NEC infrared (IR) remote control signals using the ATTiny13 microcontroller. It is based on the tutorial [AVR ATTiny13 NEC IR Protocol Remote Control](https://www.laptrinhdientu.com/2024/10/AVR-ATTiny13-NEC-IR-Protocol-RemoteControl.html) by Nguyễn Văn Nghĩa.

The NEC protocol is widely used in remote controls for TVs, air conditioners, and other consumer electronics. This project shows how to receive and decode these signals using minimal hardware and code.

## Hardware Setup
- **Microcontroller:** ATTiny13
- **IR Receiver:** Vishay TSOP4838
- **Optional Display:** OLED (I2C, for decoded command display)

The IR receiver is connected to the ATTiny13, which processes the incoming IR signals. Optionally, an OLED display can be used to show the decoded command.

## Decoding Method
- **External Interrupts:** Used to detect signal edge changes (rising/falling) on the IR receiver output.
- **Timer:** Measures the time between signal edges to decode the NEC protocol frame.
- **Frame Structure:** The NEC protocol frame includes a start pulse, address, command, and stop bit.

## Software Design
- The code uses external interrupts to capture each edge of the IR signal.
- Timer is used to measure pulse widths, which are then interpreted according to the NEC protocol.
- The decoded command can be displayed on an OLED via I2C (optional).

## Resources
- [Project Article](https://www.laptrinhdientu.com/2024/10/AVR-ATTiny13-NEC-IR-Protocol-RemoteControl.html)
- [NEC Protocol Details](https://www.laptrinhdientu.com/2024/09/mot-so-chuan-hong-ngoai-ir-remote.html#ir2)
- [Source Code](https://github.com/nghia12a1-t-ara/AVR_Microcontrollers/blob/master/3_ATTiny13/ATTiny13_IR_NEC_Decoder/ATTiny13_IR_NEC_Decoder.c)

## Author
- Nguyễn Văn Nghĩa ([Blog](https://www.laptrinhdientu.com/), [GitHub](https://github.com/nghia12a1-t-ara), [YouTube](https://www.youtube.com/@laptrinhdientu))

