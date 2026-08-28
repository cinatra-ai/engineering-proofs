# engineering-proofs

Pictures and short recordings that prove a pull request did what it says. This
repository exists so that a proof can be **seen on the pull request** without ever
being committed to a product repository. It is an image host, nothing more.

## Rules

- One folder per pull request: `<repository>/<pull-request-number>/` — for example
  `cinatra/3061/`. File names say what the picture shows
  (`run-page-skills-row-light.png`), never a slice code.
- Only proof media: PNG, JPEG, WebP, MP4/WebM, and a short `README.md` per folder
  that lists each file with what it requires, what it shows, and the verdict.
- No product code, no test fixtures, no planning notes, no secrets. A capture that
  shows a credential, a token or a private address is not pushed — it is retaken.
- A pull request embeds the pictures by **permalink** (the `blob/<40-character
  commit sha>/…` form). Permalinks must keep working: history here is never
  rewritten, and a file cited by a merged pull request is never deleted or moved.
- Temporary, unpublished captures do not belong here either; they live in the
  developer's own working area outside every repository.

## Why

Proof artifacts inside product repositories bloated the trees, blurred what a test
fixture is, and let per-issue folders accrete. Product repositories now refuse them
mechanically; this repository carries the pictures instead, and the pull request
carries the graded checklist.
