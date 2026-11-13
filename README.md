# OC-Emulator-Disks

Prebuilt `.ocd` disk images for [OC Emulator](https://github.com/zip132sy/OC-Emulator).
The emulator reads `index.json` and downloads the images into its `disks/` folder
(menu: **System disks**). Nothing here is bundled with the emulator itself.

Some systems also need their own EEPROM boot program (EFI). It is published in
`efi/` and downloaded together with the disk; the emulator then uses it as the
EEPROM of a newly created virtual machine.

| File | System | Version | EFI |
| --- | --- | --- | --- |
| openos-1.7.5.ocd | OpenOS | 1.7.5 | — |
| mineos-new.ocd | MineOS | New | efi/mineos-new.efi |
| plan9k.ocd | Plan9k | Pipes 1.2 (installed, bootable) | — |
| fuchas.ocd | FuchasOS | 0.7.0 (installed, bootable) | efi/fuchas.efi |

`index.json` format:

```json
{
  "disks": [
    {
      "file": "name.ocd",
      "label": "Shown name",
      "system": "OpenOS",
      "version": "1.8.10",
      "size": 0,
      "sha256": "...",
      "efi": { "file": "name.efi", "size": 0, "sha256": "..." }
    }
  ]
}
```
