<p align="center"><a href="https://github.com/dihny/3DSConverters"><img src="logo.svg" alt="3DS ROM Manager" width="1000" height="1000"></a></p>
<h3 align="center">A comprehensive batch tool for managing Nintendo 3DS ROM files</h3>
<hr>

**3DS ROM Manager Suite** is an all-in-one tool for converting, decrypting, and compressing Nintendo 3DS ROM files. Built upon community tools and inspired by rohithvishaal's Python concept, this suite provides a menu-driven interface for managing your 3DS game library.

![GitHub Release](https://img.shields.io/github/v/release/dihny/3DSConverters?style=flat) ![GitHub Repo stars](https://img.shields.io/github/stars/dihny/3DSConverters?style=flat) ![Issues](https://img.shields.io/github/issues/dihny/3DSConverters?style=flat)

# Features

### Format Conversion
- **CCI/3DS to CIA**: Convert cartridge dumps to installable format with automatic encryption handling
- **CIA to CCI**: Convert installable format back to cartridge dumps (decrypted files only)
- Uses 3dsconv for optimal compatibility and firmware spoof removal
- Batch processing with visual progress bars

### Decryption Support
- **Decrypt Files**: Batch decrypt encrypted ROMs
- **Decrypt to CIA**: Decrypt and output as installable format
- **Decrypt to CCI**: Decrypt and output as cartridge format
- Integrates with Batch CIA 3DS Decryptor Redux
- Smart detection of already-decrypted files (skips `-decrypted` suffix)

### Z3DS Compression
- **Compress to Z3DS**: Create compressed files for Azahar emulator (`.z3ds`, `.zcci`, `.zcia`)
- Three compression levels: Fast (Level 1), Balanced (Level 3), Best (Level 9)
- **Decompress Z3DS**: Extract compressed files back to original format
- **View Z3DS Info**: Display detailed compression statistics

### Additional Features
- Visual progress tracking for all batch operations
- Optional source file deletion after successful operations (saves disk space)
- Session logging with detailed operation history
- File inventory browser with pagination
- Temporary file cleanup utility
- Input sanitization to prevent command injection
- Comprehensive statistics dashboard

# Installation

### Windows

Download the latest release from [Releases](https://github.com/dihny/3DSConverters/releases).

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
│   ├── seed.db
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

### Menu Options

```
 BASIC CONVERSION
 1. CCI/3DS to CIA      Cartridge to installable format
 2. CIA to CCI          Installable to cartridge format

 DECRYPTION & CONVERSION
 3. Decrypt Files       Decrypt encrypted ROMs
 4. Decrypt to CIA      Decrypt and output as CIA
 5. Decrypt to CCI      Decrypt and output as CCI

 AZAHAR EMULATOR (Z3DS FORMAT)
 6. Compress to Z3DS    Compress ROMs for Azahar
 7. Decompress Z3DS     Extract from Z3DS format
 8. View Z3DS Info      Show compressed file details

 UTILITIES
 9. List Files          Show all ROM files in folder
 10. Statistics         View session statistics
 11. Clean Temp         Remove temporary files
```

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
- Files with special characters (`&`, `|`, `<`, `>`, `^`, `!`) in the filename will be rejected for security.
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

# Disclaimer

This tool is intended for personal backup and archival purposes only. Users are responsible for complying with local laws regarding game backups and ROM files. The author does not condone or support piracy.