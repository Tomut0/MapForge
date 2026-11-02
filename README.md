# MapForge (LabAPI)

MapForge lets server owners customize SCP: Secret Laboratory maps by loading bundles and spawning supported map objects.

## This fork

Version **1.0.8** is a LabAPI compatibility build based on [Killers0992/MapForge](https://github.com/Killers0992/MapForge). It updates the plugin for LabAPI 1.1.7, Harmony 2.4.2, and the current door permission API. The upstream author and GPL-3.0 license are preserved.

Compatibility changes and this README were prepared with **OpenAI Codex**. Original MapForge code and authorship remain credited to Killers0992.

## Install

1. Download [`MapForge-labapi.dll`](https://github.com/Tomut0/MapForge/releases/latest/download/MapForge-labapi.dll) and [`MapForge.API.dll`](https://github.com/Tomut0/MapForge/releases/latest/download/MapForge.API.dll).
2. Put `MapForge-labapi.dll` in the LabAPI `plugins/<port>/` directory.
3. Put `MapForge.API.dll` in the LabAPI `dependencies/<port>/` directory.
4. LabAPI 1.1.7 provides the compatible Harmony 2.4.2 dependency; do not replace the server's shared Harmony assembly with another version.
5. Start the server. MapForge creates its own data directory under the LabAPI plugins path.

## Compatibility

| Component | Version |
|---|---:|
| SCP: Secret Laboratory dedicated server | 14.2.9 |
| LabAPI runtime | 1.1.7.0 |
| Harmony | 2.4.2 |
| Plugin | 1.0.8 |

Runtime load and enable were confirmed in server logs on **2026-11-02** with SCP:SL 14.2.9 and LabAPI 1.1.7.0 (test build 1.0.7). Version 1.0.8 is rebuilt from the same tested compatibility changes with the plugin version metadata incremented.

## Build

Build `MapForge.sln` in `LABAPI` configuration with .NET Framework 4.8 targeting tools. Set `SL_REFERENCES` to the SCP:SL and LabAPI reference assemblies. The output files are `MapForge/bin/LABAPI/MapForge-labapi.dll` and `MapForge.API/bin/LABAPI/MapForge.API.dll`.

## Credits and license

- Upstream project: [Killers0992/MapForge](https://github.com/Killers0992/MapForge)
- License: [GNU GPL v3](LICENSE.txt)
