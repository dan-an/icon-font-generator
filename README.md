# Krypto-icons
Icon font assembler

## Description
Assembles glyph font from svgs in `./vectors` for using in other projects.
Core of project is [fontcustom](https://github.com/drichner/fontcustom)
Icons 

## Usage
Font automatically assembles on push in `master`.

Common steps:
- Put svgs in `./vectors`, do not remove or rename previously added icons
- Glyph in a font will be named as target svg
- Change config in `fontcustom.yml` if needed ([read more](https://github.com/FontCustom/fontcustom/blob/master/lib/fontcustom/templates/fontcustom.yml))

Steps for assemble on push:
- Commit and push your changes to remote repo
- As your MR is accepted, font will be automatically assembled.
- Update package in your project
- Add `node_modules/krypto-icon/public/fontcustom.css` to your project
- Use new icons setting HTML element class like `.kr-{icon_name}`

Steps for manual assemble:
- Call `docker run -v ${PWD}:/project --rm drichner/fontcustom compile`
- Open `fontcustom-preview.html` to check assembled font
