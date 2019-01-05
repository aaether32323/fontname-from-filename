# fontname-from-filename

A quick and dirty script that changes font metadata using the filename.
Was made to work with [TypeRip](https://github.com/CodeZombie/TypeRip).

## Installation

```
# fff.py is a bit easier to type but use whatever you want
# I personally use a shell wrapper script.
curl -L https://git.io/vhXyO -o fff.py
chmod u+x fff.py
```

Should work on all platforms, but only tested on macOS.

## Example

```
├── Rival Black Italic.otf
├── Rival Black.otf
├── Rival Bold Italic.otf
├── Rival Bold.otf
├── Rival ExtraBold Italic.otf
├── Rival ExtraBold.otf
├── Rival Light Italic.otf
├── Rival Light.otf
├── Rival Medium Italic.otf
├── Rival Medium.otf
├── Rival Regular Italic.otf
├── Rival Regular.otf
├── Rival UltraLight Italic.otf
└── Rival UltraLight.otf
```

Say the metadata of these fonts are messed up for whatever reason, but the filenames are
correct. This script will fix that by changing records 1, 2, 4, and 6 of the [name table][1].

Works for fonts with more than one word family names if you change the `FONT_FAMILY_WORD_COUNT`
variable in the beginning of the script.
For example, if the font family is called "Source Code Pro" you should change
it to 3.

[1]: https://docs.microsoft.com/en-us/typography/opentype/spec/name

## Acknowledgements

Thanks to Chris Simpkins for his work on [fontname.py](https://github.com/chrissimpkins/fontname.py).

This code is licensed under the MIT License. Copyright (c) 2018 Aman Verma
