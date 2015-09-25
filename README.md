# Custom Windows Keyboard Layouts

## Description

Set of custom keyboard layouts for Windows.

To build the installers for those layouts use the [Microsoft Keyboard Layout Creator][2]

## Layouts

### fr-num

Invert numerical keys with special characters at the top of the keyboard so that there is no need to press the `[Shift]` key.

### en-fr

Add extra keys taken from the French AZERTY keyboards.
Most of those keys can be obtained thanks to the `[Alt Gr]` or `[Ctrl]+[Alt]` combination.
Locations of those special keys are the same as on the French AZERTY keyboard.

#### Examples

- `[Alt Gr]+[2] = "é"`
- `[Alt Gr]+[-] = "à"`
- `[Alt Gr]+[7] = "è"`
- `[Alt Gt]+[[], [E] = "ê"`
- `[Shift]+[Alt Gt]+[[], [E] = "ë"`

## Notes

Add the following to this `.git/config` or to your `~/.gitconfig`:

```
[filter "winutf16"]
	clean = iconv -f utf-16 -t utf-8
	smudge = iconv -f utf-8 -t utf-16
	required
```

## References

- [Create your own keyboard layout][1]
- [Microsoft Keyboard Layout Creator 1.4][2]

[1]: http://windows.microsoft.com/en-us/windows-vista/create-your-own-keyboard-layout
[2]: https://www.microsoft.com/en-us/download/details.aspx?id=22339