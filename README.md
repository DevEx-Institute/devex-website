# DevEx Institute website

https://devex.institute

## Details

- Hugo v0.126.1
- Theme: ported from [Hugobricks](https://github.com/jhvanderschee/hugobricks), [DEMO](https://www.hugobricks.preview.usecue.com/)

## Configuration 

### Integration steps taken

- Copied `data` from theme
- Copied `static/css` from theme
- Copied base theme files to `themes/hugobricks`
- Copied shortcode content to `content/en/bricks`
- Copied:
  - theme's `content/en/_index.md` to `content/en/index.md`
  - theme's `content/en/about.md` to `content/en/about.md`
  - theme's `content/en/contact.md` to `content/en/contact.md`
  - theme's `content/en/team.md` to `content/en/team.md`
  - theme's `themes/hugobricks/i18n/en.yaml` to `i18n/en.yaml` for base i18n + future options
- Converted `config.yaml` to `hugo.toml`

### Config options

- `./hugo.toml`: Basic configuration options for base site
- `./data/settings.yaml`: Settings for the site, i.e. favicon, cursor, etc
- `./data/en/general.yaml`: Settings for site name, description, etc
- `./data/en/header.yaml`: Settings for logo, menu, etc
- `./data/en/people.yaml`: Settings for the team display
- `./data/en/footer.yaml`: Settings for footer, social links, bottom menu, etc.
- Added `./config/production/hugo.toml` for production build settings, and included GA code
- Edited "landing page" at `./content/en/_index.md` to include what content is included on the home page
- Added `./static/css/style.css` and included override css for post titles
- Duplicated `./themes/hugobricks/layouts/partials/brick_post.html` to `./layouts/partials/` and then edited to move post image to be above the title in post view
- 

### Modifications made

- Copied `/themes/hugobricks/layouts/partials/people.html` to `./layouts/partials/people.html` and modified to add Twitter links and adjust location of social links