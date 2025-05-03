![CoDex](https://github.com/user-attachments/assets/71b75052-b5d4-4a20-a532-73e61f08206b)

# CoDeX

This package contains colorful styles for page headings, codeboxes and textboxes. Including many easy to use good looking presets that are configurable.

## Examples

![Codebox and Textbox examples](https://github.com/user-attachments/assets/5789a8c2-3e41-4ac7-abd3-075350f5ef9f)

See [Examples](Examples) for full documents.

### Codebox

```ada
\begin{cdxcodebox}{Fruity.py}{Python}
def sweet_fruits(fruits):
  for fruit in fruits:
    if fruit != "lemon": # No lemons allowed!
      print(fruit)
sweet_fruits("apple", "orange", "lemon")
\end{cdxcodebox}
```

### Textbox

```ada
\begin{cdxtextbox}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Nullam elit arcu, vestibulum in mollis non, ultrices non velit.
\end{cdxtextbox}
```

## Installation

This LaTeX package consists of only one .sty file. If you want to use the package within you current LaTeX document, just paste the `CoDeX.sty` file inside the same directory as your `.tex` file.

There are two versions of the package. Use the one you want. The first uses minted and the second one uses listings for code highlighting.
<details>
  <summary>

### CoDeX for listings 
> _RECOMMENDED - works even within Overleaf_
  </summary>

### Requirements

To compile your `.tex` files that are using this package, you need to ensure that the following requirements are correctly installed:

- **LaTeX distribution:** (e.g. TeX Live 2022+ or MiKTeX)
- **Standard LaTeX packages:**
  - amsmath, amssymb
  - tikz, graphicx, xcolor
  - fontenc
  - ifthen
- **Additional LaTeX packages:**
  - atbegshi
  - tcolorbox
  - listings
  - fancyhdr, eso-pic
  - environ, fancyvrb
  - ae, lmodern, cmbright
  - xkeyval, xparse, kvoptions
  - varwidth, needspace
  - mathastext
- **TikZ libraries:**
  - patterns, calc
</details>

> [!TIP]
> This is basically always the better version. Use this version!

<details>
  <summary>

### CoDeX for minted
> _NOT RECOMMENDED - more technically complex and platform dependent_
  </summary>

### Requirements

To compile your `.tex` files that are using this package, you need to use the `-shell-escape` compiler flag. Additionally you need to ensure that the following requirements are correctly installed:

- **LaTeX distribution:** (e.g. TeX Live 2022+ or MiKTeX)
- **Minted:** code highlighting (follow instructions from official documentation; https://ctan.org/pkg/minted)
- **Python 3:** used by minted (including pygments package; https://pygments.org)
- **Standard LaTeX packages:**
  - amsmath, amssymb
  - tikz, graphicx, xcolor
  - geometry, fontenc
  - ifthen
- **Additional LaTeX packages:**
  - ifplatform, atbegshi, filecontents
  - tcolorbox
  - minted
  - fancyhdr, eso-pic
  - environ, fancyvrb
  - ae, lmodern, fontspec, cmbright
  - xkeyval, xparse, kvoptions
  - varwidth, needspace
- **TikZ libraries:**
  - patterns, calc
</details>

> [!NOTE]
> At the moment the minted version is only tested on Windows, but it should theoretically work on Linux/macOS. This does not apply to the listings version. The listings version is platform independent.

> [!IMPORTANT]
> **Why is `-shell-escape` for minted version required?**
> This version provides options to change accent colors that will be used by minted (or more specific pygments) for code highlighting. This means that the .sty file contains a small python script that dynamically generates the needed pygments style and stores it in the default location of all built-in pygment styles. The script is embedded and not a seperate file so that you just need the single .sty file for installation and not multiple. This does not apply to the listings version. The listings version does not need `-shell-escape`.


## Documentation

See [Documentation](Documentation/V1.0.0/CoDeX_Docs_V1.0.0.pdf) for reference manual.

## License

This package is licensed under the MIT License. See the [License](LICENSE.md) file for more details.
