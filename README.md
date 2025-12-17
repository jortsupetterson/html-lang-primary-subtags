# html-lang-primary-subtags

TypeScript union type for **primary language subtags** (ISO-639 / IANA) compatible with the HTML `lang=""` attribute.

This package provides a strictly typed union of all registered **primary language subtags**, without regions, scripts, variants, or extensions.

Useful for:

- typing HTML `lang` attribute safely
- typing multilingual function params
- autocomplete of valid language codes
- avoiding invalid language identifiers at compile time

---

## Install

```bash
npm install html-lang-primary-subtags
```

## Use

```ts
import type { PrimaryLanguageSubtag } from "html-lang-primary-subtags";

const lang: PrimaryLanguageSubtag = "en"; // ok
// const invalid: PrimaryLanguageSubtag = "en-US"; // compile-time error
```

`PrimaryLanguageSubtag` is a union of all registered primary language subtags (ISO-639) suitable for the HTML `lang` attribute without region/script/variant extensions.

## Types

- `PrimaryLanguageSubtag` – primary language subtags (ISO-639-1)
- `RegionSubtag` – uppercase region codes (ISO-3166-1 alpha-2)
- `Bcp47Locale` – `${PrimaryLanguageSubtag}-${RegionSubtag}` for HTML `lang` (BCP-47)
- `OgLocale` – `${PrimaryLanguageSubtag}_${RegionSubtag}` for Open Graph tags

### Examples

```ts
import type {
  PrimaryLanguageSubtag,
  RegionSubtag,
  Bcp47Locale,
  OgLocale,
} from "html-lang-primary-subtags";

const lang: PrimaryLanguageSubtag = "en";
const region: RegionSubtag = "US";
const bcp47: Bcp47Locale = "en-US";
const ogLocale: OgLocale = "en_US";
```

## Changelog

See `CHANGELOG.md` for release notes.
