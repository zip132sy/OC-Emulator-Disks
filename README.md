# OC-Emulator-Disks

Prebuilt `.ocd` disk images for [OC Emulator](https://github.com/zip132sy/OC-Emulator).
The emulator reads `index.json` and downloads the images into its `disks/` folder
(menu: **System disks**). Nothing here is bundled with the emulator itself.

| File | System | Version |
| --- | --- | --- |
| openos-1.7.5.ocd | OpenOS | 1.7.5 |
| mineos-new.ocd | MineOS | New |

`index.json` format:

```json
{ "disks": [ { "file": "name.ocd", "label": "Shown name", "system": "OpenOS", "version": "1.8.10", "size": 0, "sha256": "..." } ] }
```
