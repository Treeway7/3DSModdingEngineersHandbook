---
title: "Load Encrypted ROMs in Citra"
weight: 4
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Load Encrypted Games in Citra

You have two options:

1. Copy the AES keys from your 3DS and import them into Citra. Works for any encrypted ROM.
2. Decrypt individual ROM files. *(64-bit Windows only)*

## Importing AES keys into Citra (Recommended)

There are AES encryption keys on your 3DS which can decrypt the ROM files on a cartridge. Citra can import these keys dumped from your 3DS and decrypt ROMs for you.

Citra's wiki describes the process of doing so.

{{< button href="https://citra-emu.org/wiki/aes-keys/" >}}View dump instructions on Citra Wiki{{< /button >}}

## Decrypting Individual ROM Files

{{<hint info>}}
This method will only work on Windows 64-bit, since the bundled decryption software is built for Windows only.
{{</hint>}}

1. Download [Batch CIA Decryptor](https://gbatemp.net/download/batch-cia-3ds-decryptor.35098/download?version=35152).
2. Extract the downloaded folder and move it to a safe location.
3. Place any encrypted ROM into this folder.
4. Double click on `Batch CIA 3DS Decryptor.bat`. This will take a moment.
5. You should now see a ROM that ends in `.decrypted.cia`. Copy this to your ROM folder!

## References

https://citra-emu.org/wiki/aes-keys/

https://gbatemp.net/threads/batch-cia-3ds-decryptor-a-simple-batch-file-to-decrypt-cia-3ds.512385/