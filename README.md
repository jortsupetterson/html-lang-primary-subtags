# html-lang-primary-subtags

TypeScript union type for **primary language subtags** (ISO-639 / IANA) compatible with the HTML `lang=""` attribute.

This package provides a strictly typed union of all registered **primary language subtags**, without regions, scripts, variants, or extensions.

Useful for:

- typing HTML `lang` attribute safely
- typing config files for multilingual sites
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

const lang: PrimaryLanguageSubtag = "fi"; // ok
// const invalid: PrimaryLanguageSubtag = "en-US"; // compile-time error
```

`PrimaryLanguageSubtag` is a union of all registered primary language subtags (ISO-639) suitable for the HTML `lang` attribute without region/script/variant extensions.
