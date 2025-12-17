# Changelog

All notable changes to this project are documented here.

## 1.1.0 - 2025-12-17

- add `Bcp47Locale` (`${PrimaryLanguageSubtag}-${RegionSubtag}`) and `OgLocale` (`${PrimaryLanguageSubtag}_${RegionSubtag}`) unions so consumers can type HTML `lang` and Open Graph locales
- fix duplicate `PrimaryLanguageSubtag` export and include missing subtags (`ae`, `ak`, `sh`) while keeping legacy ones (`bh`, `jv`)
- align package metadata and published files (MIT license, changelog, README, dist)
