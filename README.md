# Arabic Reshaper LUA
Arabic Text Reshaper by Platine

The Arabic Reshaper for WoWinArabic addons is a powerful tool that enables the reshaping of Arabic characters to improve the overall appearance and readability of text. It uses a table of reshaping rules for Arabic characters, including letters and ligatures, to ensure that the text is displayed correctly in games such as World of Warcraft or any other game that accepts Lua.

The reshaper uses the position of each letter in the text to determine the reshaping. For instance, if the letter is at the beginning of the word, it will be reshaped as an "initial" form, while if it's at the end of the word, it will be reshaped as a "final" form. The reshaper also takes into account the characters that come before and after the current one to determine the correct reshaping. Additionally, it can handle ligatures of 2 or 3 characters.

This reshaper is essential for those working with Arabic text in the gaming industry, or for anyone looking to enhance the aesthetics of their Arabic text. Developed by Platine, and based on the UTF8 library by Kyle Smith, it offers a user-friendly interface and powerful reshaping capabilities. Obtain it now and effortlessly improve the readability of your Arabic text.

<img src="https://user-images.githubusercontent.com/8531014/214683759-bc6a185b-691e-4e72-98f1-fd276412169f.png" width="500">
<img src="https://user-images.githubusercontent.com/8531014/214683771-ff7fc9d9-616a-47c3-ae57-5570c957873f.png" width="500">

## Overview

This code implements Arabic text reshaping to convert logical Arabic text to properly displayed visual Arabic text. 

Key features:

- Implements Arabic reshaping rules and ligatures
- Handles UTF-8 encoded Arabic text
- Reverses and reshapes Arabic text for right-to-left display

## Installation
To use this library, simply copy the AS_Reshaping.lua file into your project's directory and require it in your code:

## Reshaping Rules

The reshaping rules are defined in the `AS_Reshaping_Rules` table. This maps Arabic characters to their isolated, initial, middle and final forms.

Additional Arabic ligature rules are defined in `AS_Reshaping_Rules2` and `AS_Reshaping_Rules3`.

## Functions

**AS_UTF8charbytes**

Returns the number of bytes used by a UTF-8 encoded character.

**AS_UTF8len** 

Returns the number of characters in a UTF-8 encoded string.

**AS_UTF8find**

Finds a character in a UTF-8 encoded string.

**AS_UTF8sub**

Extracts a substring from a UTF-8 string based on character positions.

**AS_UTF8reverse**

Reverses a UTF-8 string and applies reshaping rules. This is the main reshaping function.

## Usage

1. Define reshaping rules in `AS_Reshaping_Rules`, `AS_Reshaping_Rules2` and `AS_Reshaping_Rules3` tables

2. Pass Arabic text string to `AS_UTF8reverse` to reshape and reverse it

3. The returned string will be properly shaped and ordered right-to-left

4. Display reshaped string in right-to-left text element

## Example

```lua
arabic_text = "السلام عليكم"

reshaped_text = AS_UTF8reverse(arabic_text) 

print(reshaped_text)

-- Output: مكيلع ملاسلا
```
## License
This library is released under the MIT License. See the LICENSE file for more information.
