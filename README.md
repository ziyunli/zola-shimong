# shimong

[![Netlify Status](https://api.netlify.com/api/v1/badges/545b20bd-ce8d-43d7-b0f7-63de2200eccf/deploy-status)](https://app.netlify.com/sites/zola-shimong/deploys)

![main page screenshot](https://github.com/ziyunli/zola-shimong/blob/main/main.png?raw=true)

![posts page screenshot](https://github.com/ziyunli/zola-shimong/blob/main/posts.png?raw=true)

## Contents

- [shimong](#shimong)
  - [Contents](#contents)
  - [Installation](#installation)
  - [Options](#options)
    - [Nav](#nav)
  - [Original](#original)

## Installation
First download this theme to your `themes` directory:

```bash
cd themes
git clone https://github.com/ziyunli/shimong
```
and then enable it in your `config.toml`:

```toml
theme = "shimong"
```

This theme requires your organizes your posts in a `content/posts` folder, where you should also have an `_index.md` file with the following content:

```md
+++
title = "Posts"
template = "list.html"
sort_by = "date"
generate_feed = true
+++
```

The theme requires tags and categories taxonomies to be enabled in your `config.toml`:

```toml
taxonomies = [
    # You can enable/disable RSS
    {name = "categories", feed = true},
    {name = "tags", feed = true},
]
```

## Options

### Nav
Set a field in `extra` with a key of `shimong_menu`:

```toml
shimong_menu = [
    {url = "$BASE_URL/posts", name = "blog"},
    {url = "$BASE_URL/about", name = "about"},
    {url = "$BASE_URL/categories", name = "categories"},
    {url = "$BASE_URL/tags", name = "tags"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

## Original
This template is based on the Hugo template https://git.sr.ht/~emersion/emersion.fr/tree/master/item/themes/shimong
