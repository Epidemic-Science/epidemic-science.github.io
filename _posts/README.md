# News items

Each file in this folder is one news item. It shows on the home page ("Latest news", newest 5),
on the News page (`/news/`), on its own page, and in the RSS feed (`/feed.xml`).

## Adding an item

1. Create a file named `YYYY-MM-DD-short-title.md`, e.g. `2026-11-20-new-postdoc.md`.
   The date in the file name is the item's date.
2. Start it with this front matter, then write the text in Markdown below it:

```
---
title: "Welcome to our new postdoc"
lab: ceph                  # one lab id, or a list: [ceph, seal]
kind: paper                # optional: paper or preprint (see below)
venue: PNAS                # journal or preprint server, used with kind
image: /images/news/new-postdoc.jpg   # optional, landscape, under 500 KB
image_alt: "Short description of the photo"
link: https://doi.org/...  # optional button at the end (e.g. the paper)
link_text: Read the paper  # optional; default is "Read the paper"
---

The first paragraph is used as the summary on the News page, so make it a complete sentence.
```

Lab ids are the ones in `_data/labs.yml` (`ceph`, `seal`, `mcore`).

## Papers and preprints

For a paper or preprint, put the paper's own title in `title` and add `kind` and `venue`.
The headline is then written for you, so all items follow the same pattern:

| Front matter | Headline shown |
|---|---|
| `kind: paper`, `venue: PNAS` | Published in *PNAS*: <title> |
| `kind: preprint`, `venue: medRxiv` | Preprint available at *medRxiv*: <title> |

Leave `kind` out for any other news (new members, awards, events); the title shows as written.
