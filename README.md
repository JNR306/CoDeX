![CoDex](https://github.com/user-attachments/assets/71b75052-b5d4-4a20-a532-73e61f08206b)

# CoDeX

This package contains colorful styles for page headings, codeboxes and textboxes. Including many easy to use good looking presets that are configurable.

## Examples

> _currently not available_

## Installation

This LaTeX package consists of only one .sty file. If you want to use the package within you current LaTeX document, just paste the CoDeX.sty file inside the same directory as your .tex file.

> [!NOTE]
> At the moment the package is only tested on Windows, but it should theoretically work on Linux/macOS.

### Requirements

To compile your .tex files that are using this package, you need to use the '-shell-escape' compiler flag. Additionally you need to ensure that the following requirements are correctly installed:

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
> [!IMPORTANT]  
> #### Why is '-shell-escape' required?
> This package provides options to change accent colors that will be used by minted (or more specific pygments) for code highlighting. This means that the .sty file contains a small python script that dynamically generates the needed pygments style and stores it in the default location of all built-in pygment styles. The script is embedded and not a seperate file so that you just need the single .sty file for installation and not multiple.

## Documentation

> _currently not available_
