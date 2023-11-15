# MicroPython SSD1306 OLED Driver with Text Size Customization

This repository contains a modified version of the MicroPython SSD1306 OLED driver (`ssd1306.py`). The primary enhancement in this version is the ability to write text to the screen in various sizes.

## Original Source

The original code is derived from the micropython-lib repository. All credits for the original code go to the micropython-lib contributors.

- Original Repository: [micropython-lib on GitHub](https://github.com/micropython/micropython-lib)
- License: MIT License (Please refer to the [LICENSE](https://github.com/micropython/micropython-lib/blob/main/LICENSE) file in the original repository for details.)

## Usage

To use the enhanced functionality, follow these steps:

1. Import the modified `ssd1306.py` module.
2. Initialize the SSD1306 object.
3. Utilize the `write_text` method to display text with different sizes.

### Example

```python
from machine import I2C, Pin
from ssd1306 import SSD1306_I2C

# Initialize I2C
i2c = I2C(0, scl=Pin(9), sda=Pin(8), freq=400000)

# Initialize SSD1306 with width, height, I2C interface, and optional parameters
oled = SSD1306_I2C(128, 64, i2c)

# Display text with different sizes
oled.write_text("Hello, MicroPython!", x=0, y=0, size=2)
oled.write_text("Customizable Text!", x=0, y=20, size=3)
```

## License

The original code is licensed under the MIT License. Please refer to the [LICENSE](LICENSE) file for details.
