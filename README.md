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
  - theme's `content/en/_index.md` to `content/en/_index.md`
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
- Added `./netlify.toml` for Netlify build settings
- Updated `./data/en/footer.yaml` with copyright and theme info

### Modifications made

- Copied `/themes/hugobricks/layouts/partials/people.html` to `./layouts/partials/people.html` and modified to add Twitter links and adjust location of social links
- Edited "landing page" at `./content/en/_index.md` to include what content is included on the home page
- Added `./static/css/style.css` and included override css for post titles
- Duplicated `./themes/hugobricks/layouts/partials/brick_post.html` to `./layouts/partials/` and then edited to move post image to be above the title in post view
- Multiple css changes made in `/static/css/style.css`
- Adjusted recent posts on home page to not have a filter
- Added `load more posts` button to end of Recent Posts
- Updated `canonical_url` usage in theme by moving `<head></head>` elements into a partial at `./layouts/partials/head.html` and then including it in the `baseof.html` layout, and then adding logic for if `canonicalUrl` is used in the front matter of a post
- Updated `archetypes/default.md` to meet the necessary elements for a new post (use `hugo new content posts/<name-of-new-post>.md`)
- Created `./layouts/partials/brick_about.html` as a custom brick based off of `image2` brick, and kept About on home page
- Utilizing contact form on home page instead of separate page
- Added Google Analytics to `./layouts/partials/head.html` and it will only display on production builds

