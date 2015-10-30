# Custom Windows Keyboard Layouts

## Description

Set of custom keyboard layouts for Windows.

## Layouts

### kbdfrinu - French with inverted top number keys

Invert numerical keys with special characters at the top of the keyboard so that
there is no need to press the <kbd>Shift</kbd> key.

### kbdusfr - US with French AZERTY special keys

Add extra keys taken from the French AZERTY keyboards.

Most of those keys can be obtained thanks to the <kbd>Alt Gr</kbd> or
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> combination.

Locations of those special keys are the same as on the French AZERTY keyboard.

#### Examples

- <kbd>Alt Gr</kbd> + <kbd>2</kbd> = é
- <kbd>Alt Gr</kbd> + <kbd>0</kbd> = à
- <kbd>Alt Gr</kbd> + <kbd>7</kbd> = è
- <kbd>Alt Gt</kbd> + <kbd>[</kbd>, <kbd>E</kbd> = ê
- <kbd>Shift</kbd> + <kbd>Alt Gt</kbd> + <kbd>[</kbd>, <kbd>E</kbd> = ë

### kbddechext - German (Switzerland) - Extended

Add key to enter German ß letter <kbd>Alt Gr</kbd> + <kbd>S</kbd>. 

Add keys for writing most other western European languages including Norwegian,
Swedish and Spanish. 

#### Examples

- <kbd>Alt Gr</kbd> + <kbd>A</kbd> = æ
- <kbd>Alt Gr</kbd> + <kbd>N</kbd> = ñ
- <kbd>Alt Gr</kbd> + <kbd>°</kbd> is a dead key, it generates:
    * with <kbd>A</kbd> = å
    * with <kbd>Shift</kbd> + <kbd>A</kbd> = Å
- <kbd>Alt Gr</kbd> + <kbd>o</kbd> is a dead key, it generates:
    * with <kbd>E</kbd> = œ
    * with <kbd>Shift</kbd> + <kbd>E</kbd> = Œ
    * with <kbd>-</kbd> = ø
    * with <kbd>_</kbd> = Ø

## Building keyboard layout installers

To build the installers for those layouts use the [Microsoft Keyboard Layout Creator][2].

To be able to build the installer you may need to uninstall an existing layout
that has the same name (e.g. Previous version of the keyboard layout).

If that layout is actually your default one then you must select another layout
as the default to be able to uninstall that layout. 

## Cloning the Git repository

The [Microsoft Keyboard Layout Creator][2] generates UTF-16LE files.

Therefore to be able to check-in those files as text files into the Git repository,
they need to be converted to UTF-8.

To convert the UTF-16LE files, add the following to your `~/.gitconfig` or
to the cloned repository `.git/config`:

```ini
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
