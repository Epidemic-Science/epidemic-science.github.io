# Epidemic Science Hub: Image Guidelines

This folder holds every image used on the Hub website. Following these conventions (shared with the CEPH Lab
site) keeps the site fast and consistent.

## Naming

Use clear, lowercase filenames with hyphens between words and no spaces or special characters, e.g.
`marco-ajelli.jpg`.

## Folders

* `people/` — portraits for the People page. `placeholder.svg` is shown for anyone without a photo.
* `labs/` — lab logos, referenced from `_data/labs.yml`.
* top level — the Hub logo, favicon, and any banner images.

## People photos

* Crop to a square (1:1). The People page shows photos at a 5:4 ratio, cropped from the centre.
* Compress to under 1 MB.
* Reference the file from `_data/people.yml`, e.g. `image: /images/people/firstname-lastname.jpg`.

## Logos

Keep logos as PNG (or SVG) so transparency is preserved against the header and footer backgrounds. Set the Hub
logo with `logo:` in `_config.yml`.
