# Arabic Reshaper LUA
Arabic Text Reshaper by Platine

The Arabic Reshaper for WoWinArabic addons is a powerful tool that enables the reshaping of Arabic characters to improve the overall appearance and readability of text. It ues a table of reshaping rules for Arabic characters, including letters and ligatures, to ensure that the text is displayed correctly in games such as World of Warcraft or any other game that accepts Lua.

The reshaper uses the position of each letter in the text to determine the reshaping. For instance, if the letter is at the beginning of the word, it will be reshaped as an "initial" form, while if it's at the end of the word, it will be reshaped as a "final" form. The reshaper also takes into account the characters that come before and after the current one to determine the correct reshaping. Additionally, it can handle ligatures of 2 or 3 characters.

This reshaper is essential for those working with Arabic text in the gaming industry, or for anyone looking to enhance the aesthetics of their Arabic text. Developed by Platine, and based on the UTF8 library by Kyle Smith, it offers a user-friendly interface and powerful reshaping capabilities. Obtain it now and effortlessly improve the readability of your Arabic text.

<img src="https://user-images.githubusercontent.com/8531014/214683759-bc6a185b-691e-4e72-98f1-fd276412169f.png" width="500">
<img src="https://user-images.githubusercontent.com/8531014/214683771-ff7fc9d9-616a-47c3-ae57-5570c957873f.png" width="500">


## Installation
To use this library, simply copy the AS_Reshaping.lua file into your project's directory and require it in your code:

```lua
local AS_Reshaping = require("AS_Reshaping")
```
## Usage
To reshape Arabic text, call the AS_reshaping() function and pass it a string of Arabic text. The function returns the reshaped text as a string.

```lua
local reshaped_text = AS_Reshaping.AS_reshaping("اللغة العربية هي لغة جميلة")
print(reshaped_text)
Output: ﺔﻴﻟﺮﻌﻟا ﺔﻴﺒﺭﻷا ﻩﻮﻟﺍ ﺔﺳﻮﻠﻋ جميلة لغة هي عربية ال
```
To reverse the order of letters in a UTF-8 encoded string, call the AS_UTF8reverse() function and pass it the string. The function returns the reversed string.

```lua
local reversed_text = AS_Reshaping.AS_UTF8reverse("اللغة العربية هي لغة جميلة")
print(reversed_text)
Output: ةيلمج ةغل ليه يبرععلا ةيلغلا
```

## License
This library is released under the MIT License. See the LICENSE file for more information.
