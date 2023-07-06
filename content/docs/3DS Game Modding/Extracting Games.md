---
title: "Extracting ROM Files"
weight: 3
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Extracting ROM Files

## Prerequisites
- 3DS ROM ripped from a [homebrewed 3DS](/docs/3ds-game-modding/3ds-homebrew-guide/)
- [CTRTool](https://github.com/3DSGuy/Project_CTR/releases)
- Some [computer terminal](/docs/appendix/using-the-terminal/) knowledge

## Dumping the ROM File

{{< button relref="/docs/3DS Game Modding/Dumping Titles and Game Cartridges.md" >}}Dumping Titles and Game Cartridges{{< /button >}}


## Setup

1. Create a new folder on your computer (called the working folder).
2. Copy the `.cia` ROM from your SD card - `/gm9/out/*.cia` - to the working folder.
3. Extract the CTRTool folder.
4. Copy `ctrtool.exe` to the working folder.

## Extracting the ROM

CTRTool is a *command-line tool,* meaning we will need to use the terminal to run it.

1. Run Powershell.
2. Navigate to the working folder.
3. Type the following command, and replace `[rom file]` with your dumped 3DS ROM:

```
./ctrtool --contents=contents [rom file]
```

This will dump the ROM's `.app` files inside of `contents/`. These apps include the game itself, along with its digital manual.

4. One of the `.app` files within `contents/` contains your game's title ID in the filename.

Find the right `.app` file, and run the following command on it, replacing `[.app]`:

```
./ctrtool --romfsdir=romfs --exefsdir=exefs --exheader=exheader.bin [.app]
```

If successful, you should now have `romfs/` and `exefs/` folders in your working directory, as well as an `exheader.bin`!

## Troubleshooting

### "Unknown file."

You are using an old version of CTRTool, likely distributed from a third party source. Download the latest version of CTRTool from their official GitHub page.

{{< button href="https://github.com/3DSGuy/Project_CTR/releases" >}}Download CTRTool{{< /button >}}

## References

https://nsmbhd.net/thread/4635-how-to-dump-and-extract-cia-files-tutorial/