# CoolKid’s Archive Website

![Preservation status](https://img.shields.io/badge/status-partial%20restoration-2145a3)
![Recovered program](https://img.shields.io/badge/recovered%20programs-1-2d8a4d)
![Archived URLs](https://img.shields.io/badge/indexed%20URLs-247-6d4cc2)

A working preservation and restoration of **CoolKid’s Site**, originally hosted at `coolkid.text2k.net`. The project recreates the recognizable early-2000s design, repairs navigation, preserves recovered artwork and pages, documents the site’s history, and clearly separates recovered downloads from files that are still unavailable.

> **Live restored site:** [Open CoolKid’s Archive Website](https://coolkid-restored-rice2k.christopher-sc82038.chatgpt.site)  
> The deployed site is owner-private. Access has not been made public.

![Restored CoolKid homepage](docs/screenshots/restored-homepage.jpg)

## Archive at a glance

| Collection | Status |
| --- | --- |
| Restored pages | 30 main pages plus historical-path aliases |
| Indexed original URLs | 247 successful Wayback capture records |
| Original HTML recovered | 4 content-bearing documents |
| Original images recovered | Banner plus 4 program screenshots |
| Program packages recovered | 1 verified ZIP: SuperPokémon! v2.0 |
| Known unrecovered programs | SuperPokémon! v1.0, Compilation Edition, QuickBust, CoolKid Chat Tools, two address-upgrade executables, and the unconfirmed v3 release |
| Homepage news | Original bodies unavailable; restoration summaries are labeled |

## Screenshots

### Original program images

| SuperPokémon! v1 | SuperPokémon! v2 | QuickBust | CoolKid Chat Tools |
| --- | --- | --- | --- |
| ![SuperPokémon v1 screenshot](public/assets/screen-v1.gif) | ![SuperPokémon v2 screenshot](public/assets/screen-v2.gif) | ![QuickBust screenshot](public/assets/screen-qb.gif) | ![CoolKid Chat Tools screenshot](public/assets/screen-cct.gif) |

These small GIFs are preserved original site assets—not modern recreations. Their original URLs, source locations, file sizes, and SHA-256 values are recorded in the preservation manifest.

## Restored sections

- Home, News & History, Downloads, Sources, and Site Timeline
- SuperPokémon!, QuickBust, and CoolKid Chat Tools program areas
- CoolKid biography/contact records and Other/Awards pages
- Message Board category records and inactive legacy-service explanations
- Searchable download catalog with recovered/unavailable filters
- Historical file paths that lead to a real download or a clear preservation notice

## Download recovery status

### Recovered and verified

**SuperPokémon! v2.0** is preserved at [`public/downloads/superpokemonv2.zip`](public/downloads/superpokemonv2.zip).

- Size: `1,987,333 bytes`
- SHA-256: `1b450430c2c7b30be9d0ca3081dabbceaedc1ad74d2ca063a5099feec1b30e38`
- MD5: `73d3b4fff22a31ce18838eecde8acff6`
- SHA-1: `82e1bf8f73daa900b25243800bfa0ff664054840`
- ZIP members: `SuperPokemon2.CAB`, `Setup.lst`, and `setup.exe`
- Validation: archive size, MD5, and SHA-1 match Internet Archive metadata; every member passes ZIP CRC validation

This copy is not claimed to be byte-identical to the historical `SP_v2.zip`, because no checksum for the original site payload has been recovered. No executable was run.

### Unavailable or unconfirmed

Dead historical download paths are represented by information pages. They are **not** replaced with unrelated files or fabricated downloads. See [Recovery Status](docs/RECOVERY-STATUS.md) for the complete table and research notes.

## Original URLs and preserved sources

- [Complete Original URL Index](docs/ORIGINAL-URLS.md) — all 247 successful capture records, including pages, forum posts, images, scripts, and downloadable-file paths
- [Capture inventory (JSON)](public/archive/capture-inventory.json) — timestamp, original URL, MIME type, response status, digest, and archived length
- [Preservation manifest](public/archive/preservation-manifest.json) — recovered files, hashes, original URLs, research sources, and limitations
- [Site page manifest](public/archive/site-pages.json) — restored local destinations
- [Validation report](public/archive/validation.json) — generated integrity and link checks
- [Evidence directory](evidence) — recovered original HTML and retrieval logs

Primary research links:

- [April 8, 2000 original frameset](https://web.archive.org/web/20000408144135/http://coolkid.text2k.net/)
- [April 28, 2001 CoolKid section and navigation](https://web.archive.org/web/20010428092959/http://coolkid.text2k.net/ck/)
- [July 31, 2001 SuperPokémon address-upgrade page](https://web.archive.org/web/20010731132510/http://coolkid.text2k.net/programs/sp/addup.html)
- [July 28, 2001 awards page](https://web.archive.org/web/20010728110500/http://coolkid.text2k.net/other/awards.html)
- [Wayback CDX capture inventory query](https://web.archive.org/cdx/search/cdx?url=coolkid.text2k.net&matchType=prefix&output=json&filter=statuscode:200&collapse=urlkey)
- [Recovered CoolKid image collection](https://github.com/rice2k/AOL-Progz/tree/main/assets/web-resources/coolkid-text2k-net)
- [SuperPokémon! v2.0 preservation item](https://archive.org/details/superpokemonv2)

## What could not be restored

This is a **partial content restoration**, not a complete mirror. The original `main.html` and `index.shtml` homepage bodies could not be retrieved after repeated normal and raw Wayback replay attempts. The News page therefore uses clearly marked editorial summaries derived from surviving evidence. Unrecovered binaries, missing page bodies, retired CGI functions, and historical advertising/tracking services have explanatory records instead of invented content.

Four content-bearing original HTML documents were recovered: the April 8, 2000 frameset, April 28, 2001 CoolKid section, July 28, 2001 awards page, and July 31, 2001 address-upgrade page. Program titles and links are also corroborated by preserved crawl records.

## Run and validate locally

Python 3 is sufficient; there are no frontend dependencies.

```sh
python3 build.py
python3 validate.py
python3 serve.py --host 0.0.0.0 --port 3000
```

`public/` contains the generated website, `dist/` is the deployment output, and `evidence/` contains the supporting research. `validate.py` checks local links and fragments, image and binary hashes, and ZIP integrity.

## Preservation policy

- Recovered files retain source and checksum information.
- Indexed-only URLs are not described as recovered content.
- Missing programs remain labeled unavailable until a defensible copy is found.
- Original identity and graphics belong to their respective creators.
- Modern navigation, summaries, responsive behavior, and recovery notes are restoration additions by Rice2k.
- The hosted restoration remains private until Christopher approves broader access.

Restoration prepared for **Rice2k** on September 13–14, 2026.

## Related Rice2K projects

The historical restoration documents recovered pages and missing files. Its separately hosted restored demo is currently owner-private; the public repository is the available research entry point.

[Old Free Online Resources](https://github.com/rice2k/old-free-online-resources) · [AOL Progz preservation](https://github.com/rice2k/AOL-Progz) · [Search public web archives](https://rice2k.github.io/rice2k-startdeck/projects/?category=Web%20Archives)
