# Pneumatic

Pneumatic is a minimalistic, responsive [Pelican] theme. The name was chosen
because it's based on the [Skeleton] framework, and pelicans (like most birds)
possess [skeletal pneumaticity]. See the theme in action at **[kevinyap.ca]**.

![Pneumatic Screenshots](.github/screenshots.png?raw=true)

> _Note: the current version of Pneumatic uses the newly-popularized [system font
stack]. To use the older version of the theme whose font stack was based on
Google Fonts, refer to [`pneumatic@v1.0`]._


## Requirements

Pneumatic requires [Sass] and two Pelican plugins: [Neighbours] and [Assets].

## Configuration

- Create a directory containing all of the [relevant icons]. Set `ICONS_PATH`
  to that directory's path (ex. `images/icons`) and ensure that it has been
  added to `STATIC_PATHS`.
- There are intentionally no author, category, and tag page templates, so
  `AUTHORS_SAVE_AS`, `CATEGORY_SAVE_AS`, `CATEGORIES_SAVE_AS`, and
  `TAGS_SAVE_AS` should all be set to `''`.
- [`pygments.css`] can be modified to change the code block colour scheme.
- Some font and colour choices can be customized in [`pneumatic.scss`].
- CodeHilite line numbers should be enabled in Pelican's configuration file:

  ```python
  # Pelican 3.7+
  MARKDOWN = {
      'extension_configs': {
          'markdown.extensions.codehilite': {'linenums': None}
      }
  }

  # Pelican 3.6 and older
  MD_EXTENSIONS = ['codehilite(linenums=None)']
  ```

Here are theme-specific settings that should be present in the Pelican configuration file:

|  Setting            | Description                                            |
|:-------------------:|--------------------------------------------------------|
| `SITENAME`          | Text displayed under avatar in sidebar                 |
| `BIO_TEXT`          | Text displayed under site name                         |
| `FOOTER_TEXT`       | Text displayed in site footer                          |
| `ICONS_PATH`        | Location of site icons (ex. `images/icons`)            |
| `SITE_AUTHOR`       | Used for author `<meta>`                               |
| `TWITTER_USERNAME`  | Used for Twitter Cards `<meta>`                        |
| `GOOGLE_PLUS_URL`   | Used for Google+ `<meta>`                              |
| `INDEX_DESCRIPTION` | Used for description `<meta>` on index page            |
| `SIDEBAR_LINKS`     | List of anchor elements to be displayed under bio text |
| `GOOGLE_FONTS`      | List of fonts to import from Google Fonts (optional)   |
| `SOCIAL_ICONS`      | List of tuples in the form `(link, title, icon-class)` |
| `THEME_COLOR`       | Primary colour of the site (ex. `#000000`)             |
| `DISQUS_SITENAME`   | Disqus shortname (optional)                            |
| `GOOGLE_ANALYTICS`  | Google Analytics tracking code (optional)              |
| `DOMAIN`            | Used for Google Analytics and Twitter Cards `<meta>`   |
| `FA_EMBED_CODE`     | Font Awesome CDN embed code (optional)                 |


## License

Pneumatic is licensed under the [MIT License].

[Pelican]: http://getpelican.com
[Skeleton]: http://getskeleton.com
[skeletal pneumaticity]: http://en.wikipedia.org/wiki/Skeletal_pneumaticity
[kevinyap.ca]: http://kevinyap.ca

[system font stack]: https://css-tricks.com/snippets/css/system-font-stack/
[`pneumatic@v1.0`]: https://github.com/iKevinY/pneumatic/tree/v1.0

[Sass]: http://sass-lang.com
[Neighbours]: https://github.com/getpelican/pelican-plugins/tree/master/neighbors
[Assets]: https://github.com/getpelican/pelican-plugins/tree/master/assets

[relevant icons]: https://github.com/iKevinY/iKevinY.github.io/tree/src/content/images/icons
[`pygments.css`]: static/pygments.css
[`pneumatic.scss`]: static/pneumatic.scss

[MIT License]: LICENSE
