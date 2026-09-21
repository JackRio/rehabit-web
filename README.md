# Rehabit — web build

Generated output. This repository holds the **compiled static site** for the
Rehabit physiotherapy app, published with GitHub Pages. Nothing here is edited
by hand — every file is produced by `npm run build:web` from the private
source repository and committed as a single deploy commit.

## How to read this repo

- **`main`** is whatever is live right now. GitHub Pages serves from it.
- **`vX.Y.Z` tags** are immutable snapshots of every release that has been
  deployed. To see or restore an earlier site, check out its tag.
- Each deploy commit names the source commit it was built from, so any live
  file can be traced back to the code that produced it.

## Notes on the build

Routes are pre-rendered to real HTML files (`web.output: "static"`).
`404.html` is a copy of the not-found page so dynamic routes such as
`/patient/exercise/<id>` hydrate and resolve client-side, and `.nojekyll`
stops GitHub Pages from stripping the `_expo/` bundle directory.
