# basekitbrand.com

Official brand guidelines for the BaseKit platform

## Contents
- [Installation](#installation)
- [Site navigation](#site-navigation)
- [Using includes](#using-includes)
- [Page layouts](#page-layouts)
- [Page options](#page-options)

## Installation

1. Install bundler with `$ gem install bundler`
2. Install gems with `$ bundle install`
3. Run Jekyll with `$ bundle exec jekyll serve --watch`
4. View the local site at [http://localhost:4000](http://localhost:4000)

## Site navigation
There are 4 different navigation types:
- `navigation_header`: The navigation shown in the header
- `navigation_aside`: The navigation shown in the sidebar
- `social_links`: The social icon links shown at the bottom of the sidebar
- `navigation_footer`: The navigation shown in the footer

The `social_links` properties should either be one that is already in the list (so `Twitter` or `Facebook`) or simply `link`, this is so an icon can be set for the link.

## Using includes

There are 2 main types of includes: ones designed for the site and ones that are designed as shortcodes. Here are a list of the shortcode includes:

### `button.html`
A button that can link to a page of any kind.

Example usage: `{% include button.html text="I'm a button" link="https://daviddarnes.com" %}`

Available options:
- `text`: The text of the button _required_
- `link`: The link that the button goes to _required_
- `icon`: The icon that is added to the end of the button text
- `color`: The color of the button

### `figure.html`
An image with optional caption.

Example usage: `{% include figure.html image="/uploads/feature-image.jpg" caption="Check out my photo" %}`

Available options:
- `image`: The image shown _required_
- `caption`: A caption to explain the image
- `position`: The position of the image. `left`, `right` or `full`

### `icon.html`
An icon.

Example usage: `{% include icon.html id="twitter" %}`

Available options:
- `id`: The reference for the icon _required_
- `title`: The accessible label for the icon
- `color`: The desired colour of the icon

### `video.html`
A YouTube video.

Example usage: `{% include video.html id="zrkcGL5H3MU" %}`

Available options:
- `id`: The YouTube ID for the video _required_

### `site-form.html`
Adds a contact form to the page.

Example usage: `{% include site-form.html %}`

This include has no options. Use the `email` option in the `/_config.yml` to change to the desired email.

### `site-search.html`
Adds a search form to the page.

Example usage: `{% include site-search.html %}`

This include has no options. This include will add a block of javascript to the page and javascript reference in order for the search field to work correctly.

## Page layouts

- `page`: The most common layout for the site, Places content on the right and sidebar on the left
- `home`: Removes the aside entirely, leaving the full width for the main content (typically used for home page designs)
- `search`: Adds a search field to the page as well as a simplified version of the sidebar to allow more focus on the search results

## Page options

- `indexing: false`: Adds a `noindex` meta element to the `<head>` to stop crawler bots from indexing the page, used on the 404 page
