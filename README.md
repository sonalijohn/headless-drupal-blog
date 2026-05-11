# Headless Drupal Blog

A decoupled/headless Drupal 11 blog — Drupal manages content via JSON:API, consumed by a React frontend.

## Architecture
## Features

- **Drupal 11 backend** — Blog Post content type with author, summary, body, tags
- **JSON:API** — Drupal's built-in API serves content at `/jsonapi/node/blog_post`
- **React frontend** — fetches live from JSON:API, no page reload
- **Card UI** — responsive blog listing with click-through to full post
- Custom `headless_blog` Drupal module for content type setup

## Local Setup

```bash
git clone https://github.com/sonalijohn/headless-drupal-blog.git
cd headless-drupal-blog
ddev start
ddev composer install
ddev drush site:install --account-name=admin --account-pass=admin -y
ddev drush en headless_blog jsonapi -y
ddev drush cr
```

Visit frontend: `https://headless-drupal-blog.ddev.site/blog.html`

Visit JSON:API: `https://headless-drupal-blog.ddev.site/jsonapi/node/blog_post`

## Tech Stack

- Drupal 11 · PHP 8.2 · MySQL · JSON:API · React · DDEV

## Author

**Sonali John** — Drupal & PHP Full Stack Developer
[LinkedIn](https://www.linkedin.com/in/sonali-john-a707a4117/) · [GitHub](https://github.com/sonalijohn)
