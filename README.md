# Epidemic Science Hub website

Source for **https://epidemic-science.github.io**, the website of the Epidemic Science Hub at the Indiana
University School of Public Health - Bloomington. The Hub brings together three labs: the
[CEPH Lab](https://ceph-lab.github.io), the SEAL Lab, and the MCORE Lab.

The site currently uses the same stack and look as [ceph-lab.github.io](https://github.com/CEPH-Lab/ceph-lab.github.io):
[Jekyll](https://jekyllrb.com) with the `minima` theme, built and hosted by GitHub Pages.

## Updating content

Most updates are edits to the YAML files in `_data/`; the pages read from them automatically.

| To change... | Edit |
| --- | --- |
| Lab names, leads, summaries, websites, emails | `_data/labs.yml` |
| People (grouped by lab on the People page) | `_data/people.yml` + a photo in `images/people/` |
| Research theme cards | `_data/research.yml` |
| Site title, navigation order, header logo | `_config.yml` |
| Colours for the whole site | the variables at the top of `assets/main.scss` |
| Home page text (hero, Mission, What we do) | `index.html` |
| Join Us / Contact text | `join-us.html`, `contact.html` |

Search the repo for `TODO` to find every placeholder that still needs real content.

### Adding a person

1. Add a square photo (under 1 MB) to `images/people/`, named `firstname-lastname.jpg` (see `images/README.md`).
2. Add an entry to `_data/people.yml`:

   ```yaml
   - name: Firstname Lastname
     role: PhD Student
     lab: ceph            # ceph, seal or mcore
     image: /images/people/firstname-lastname.jpg
     profile: https://ceph-lab.github.io/people/firstname-lastname/   # optional
   ```

   Set `alumni: true` to move someone to their lab's Alumni list.

### Adding a logo

Put the image in `images/` and set `logo: /images/your-logo.png` in `_config.yml`. It replaces the text
wordmark in the header and footer. Lab logos go in `images/labs/` and are set per lab in `_data/labs.yml`.

## Repository layout

```
_config.yml          site settings and navigation
_data/               labs.yml, people.yml, research.yml (the site's content)
_includes/           header, footer, favicon tags, and the reusable lab card
assets/main.scss     shared styles and colour variables
images/              logos, favicon, people photos (see images/README.md)
index.html           Home
labs.html            Labs
people.html          People
research.html        Research
join-us.html         Join Us
contact.html         Contact
404.html             Not-found page
```

## Publishing

GitHub Pages rebuilds the site on every push to `main` (usually within a minute or two). If it is not live
yet: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.

## Previewing locally (optional)

With Ruby installed:

```bash
gem install bundler jekyll minima
jekyll serve
```

Then open http://localhost:4000. Restart `jekyll serve` after editing `_config.yml`.
