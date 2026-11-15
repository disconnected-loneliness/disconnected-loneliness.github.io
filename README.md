# Disconnected website

Website of the Disconnected project (NWA.1572.21.012). It is a Jekyll site: GitHub Pages builds it automatically, so nothing needs to be installed.

## Publishing on GitHub Pages

1. Create a repository on github.com and upload the contents of this folder (the folder itself is the root of the repository).
2. In the repository, go to Settings > Pages, choose "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site appears after a minute or two at `https://<account>.github.io/<repository>/`.
4. In `_config.yml`, set `baseurl` to `"/<repository>"`. Leave it empty if the repository is named `<account>.github.io` or if the site has its own domain.

## Adding a news post

1. Copy `_template-nieuwsbericht.md` into `_posts/` and name it `YYYY-MM-DD-short-title.md`.
2. Fill in the title, date, and summary at the top, and write the text below the second `---`.
3. For a photo, put the file in `assets/img/news/` and refer to it in the `image` line. Photos of about 1600 pixels wide work well.
   A post without a photo is fine: delete the three `image` lines. The home page shows the three most recent posts that have a photo.
4. For the English version, do the same in `en/_posts/`, and add the `permalink` and `alt` lines as in the existing English posts. The `alt` line links the Dutch and English versions to each other.

If a wide photo is cut off badly in the overviews, add a `thumb` line with a separate 3:2 version of the photo (see the Reinier de Graaf post).

To show only the month and year of a post (for example when the exact day is not known), add the line `month_only: true`.

All of this can be done in the browser on github.com (Add file > Create new file or Upload files).

## Changing other content

| What | Where |
|---|---|
| Team members | `_data/team.yml`, photos in `assets/img/team/` |
| Publications, data, software | `_data/publications.yml` |
| Partners | `_data/partners.yml`, logos in `assets/img/logos/` |
| Home page texts and photo | top of `index.html` and `en/index.html` |
| About page | `over.md` and `en/about.md` |
| Menu and footer text | `_data/i18n.yml` |
| Colours and fonts | `assets/css/style.css` |
| Logo and browser-tab icon | `assets/img/logo/` |

The fonts (Newsreader and Instrument Sans, both under the SIL Open Font License) are included in `assets/fonts/`, so the site loads nothing from other servers.
