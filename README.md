[![3DS ROM Manager](logo.svg)](https://github.com/dihny/3DSConverters)

![GitHub Release](https://img.shields.io/github/v/release/dihny/3DSConverters?style=flat)
![GitHub Repo stars](https://img.shields.io/github/stars/dihny/3DSConverters?style=flat)
![Issues](https://img.shields.io/github/issues/dihny/3DSConverters?style=flat)

**3DS ROM Manager Suite** is an all-in-one tool for converting, decrypting, and compressing Nintendo 3DS ROM files. Built upon community tools and inspired by rohithvishaal's Python concept, this suite provides a menu-driven interface for managing your 3DS game library.

# Features
- **Format Conversion** – Convert between .3ds, .cci, and .cia formats with batch support.
- **Decryption** – Decrypt encrypted ROMs to CIA or CCI formats.
- **Z3DS Compression** – Compress and decompress files for the Azahar emulator, with three quality levels.
- **Batch Processing** – Run operations on multiple files at once, with progress tracking.
- **Utilities** – File browser, temporary file cleanup, and session statistics.
- **Safe & User-Friendly** – Input validation, optional source deletion, and logs for all operations.

# Installation

### Windows

> 📦 **[Download Latest Release](https://github.com/dihny/3DSConverters/releases/latest)**

All required tools are included in the `bin/` directory.

**System Requirements:**
- Windows 7 SP1 (x64) or higher
- Windows Server 2008 R2 SP1 (x64) or higher
- Visual C++ Redistributable for Visual Studio 2015

### File Structure

After extraction, your directory should look like this:

```
3DS-Converters/
├── 3DS ROM Manager Suite v2.0.bat
├── bin/
│   ├── makerom.exe
│   ├── ctrtool.exe
│   ├── 3dsconv.exe
│   ├── seeddb.bin
│   ├── z3ds_compressor.exe
│   └── decrypt.exe
├── Batch CIA 3DS Decryptor Redux.bat
└── log/
    └── operations_YYYYMMDD.log
```

# Usage

1. Place ROM files (`.3ds`, `.cci`, `.cia`) in the same directory as the batch file
2. Run `3DS ROM Manager Suite v2.0.bat`
3. Select operation from the menu
4. Press Enter when prompted for filename to process all compatible files in batch mode

# Supported Formats

| Extension | Format | Description |
|-----------|--------|-------------|
| `.3ds` `.cci` | CCI | Cartridge Card Image (cartridge dumps) |
| `.cia` | CIA | CTR Importable Archive (installable format) |
| `.z3ds` `.zcci` `.zcia` | Z3DS | Compressed format for Azahar emulator |

# Notes

- CIA to CCI conversion only supports decrypted game CIAs. Encrypted files, DLC, updates, and system titles are not compatible.
- Decryption features require `Batch CIA 3DS Decryptor Redux.bat` to be present in the root directory.
- Z3DS compression features require `z3ds_compressor.exe` in the `bin/` directory.
- All operations are logged to `log/operations_[date].log` with timestamps.
- It's recommended to keep backups of important files before batch processing.

# Credits

### Development
- **Dihny** - 3DS ROM Manager Suite creator and maintainer

### Inspiration
- [**rohithvishaal**](https://github.com/rohithvishaal/3ds-converters) - Original Python-based ROM manager concept
- [**R-YaTian**](https://github.com/R-YaTian/3DS-Converters) - Prior batch script implementations

### Integrated Tools
- `Batch CIA 3DS Decryptor Redux` - [matiffeder](https://github.com/matiffeder/3DS-stuff) & [xxmichibxx](https://github.com/xxmichibxx/Batch-CIA-3DS-Decryptor-Redux)
- `makerom.exe / ctrtool.exe` - [3DSGuy](https://github.com/3DSGuy/Project_CTR) & jakcron
- `3dsconv` - [ihaveamac](https://github.com/ihaveamac/3dsconv)
- `seeddb.bin` - [ihaveamac](https://github.com/ihaveamac/3DS-rom-tools/tree/master/seeddb) & soarqin
- `z3ds_compressor` - [energeticokay](https://github.com/energeticokay/z3ds_compress)
- `decrypt.exe` - [shijimasoft](https://github.com/shijimasoft/ctrdecrypt)

Special thanks to the 3DS homebrew community for their continued development and tool maintenance.

# License

This project is released under the MIT License. Each integrated tool retains its original license - users must comply with the individual licenses of all bundled components.

>  ### ⚠️ Disclaimer:
>  This tool is intended for personal backup, archival, and educational purposes only.
>  Users are responsible for complying with local laws regarding game backups and ROM files.
>  The author does not condone or support piracy in any way.
