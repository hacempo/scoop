# hacempo/scoop

[![CI](https://github.com/hacempo/scoop/actions/workflows/ci.yml/badge.svg)](https://github.com/hacempo/scoop/actions/workflows/ci.yml)
[![Excavator](https://github.com/hacempo/scoop/actions/workflows/excavator.yml/badge.svg)](https://github.com/hacempo/scoop/actions/workflows/excavator.yml)
[![Hash Check](https://github.com/hacempo/scoop/actions/workflows/hashcheck.yml/badge.svg)](https://github.com/hacempo/scoop/actions/workflows/hashcheck.yml)

A personal [Scoop](https://scoop.sh) bucket for Windows applications.

## Add this bucket

```powershell
scoop bucket add hacempo https://github.com/hacempo/scoop
```

Install an application with:

```powershell
scoop install hacempo/<manifest-name>
```

## Available applications

| Manifest | Description |
| --- | --- |
| `bettbox` | Network debugging and traffic splitting client |
| `chrome-avx2` | Chromium optimized for AVX2 |
| `coolapk` | Unofficial Coolapk desktop client |
| `fanqie-novel-downloader` | 番茄小说下载器 |
| `junie` | JetBrains Junie CLI |
| `md3music` | Material 3 music player |
| `mpv-config` | Customized mpv configuration |
| `mtool` | Game translation and modification tool |
| `pulse` | Windows file manager |
| `qingjian` | 青简中文输入法 |
| `redpanda-cpp` | Lightweight C++ IDE |
| `screenbox` | Windows media player |
| `subtitle-finder` | Subtitle search tool |

## Automation

- **CI** validates bucket manifests on pushes and pull requests.
- **Excavator** checks for upstream releases every four hours and updates manifests.
- **Hash Check** verifies download hashes daily and repairs changed upstream assets.

Scheduled workflows can be started manually from the repository's **Actions** tab.

## Contributing

When adding or updating a manifest:

1. Include a verifiable download URL and SHA256 hash for every supported architecture.
2. Add a working `checkver` rule and matching `autoupdate` URLs whenever the upstream project supports automated version detection.
3. Preserve application data with `persist` when appropriate.
4. Validate the manifest with the repository CI before merging.

See the [Scoop App Manifests documentation](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests) for the manifest format.
