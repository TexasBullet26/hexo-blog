---
title: Example Draft
tags: [Writing, Example, Draft]
categories:
- [Example]
---
# Writing
To create a new post or a new page, you can run the following command:

```bash
$ hexo new [layout] <title>
```

`post` is the default `layout`, but you can supply your own. You can change the default layout by editing the `default_layout` setting in `_config.yml`.

### Layout
There are three default layouts in Hexo: `post`, `page`, and `draft`. Files created by each of them is saved to a different path. Newly created posts are saved to the `source/_posts` folder.

`post` -> `source/_posts`
`page` -> `source`
`draft` -> `source/_drafts`

### Drafts
Draft is a special layout in Hexo. Posts initialized with this layout are saved to the `source/_drafts` folder. You can use the `publish` command to move drafts to the `source/_posts` folder. `publish` works in a similar way to the `new` command.

```bash
$ hexo publish [layout] <title>
```

Drafts are not displayed by default. You can add the `--draft` option when running Hexo or enable the `render_drafts` setting in `_config.yml` to render drafts.

### Scaffolds
When creating posts, Hexo will build files based on the corresponding file in `scaffolds` folder. For example:

```bash
$ hexo new photo "My Gallery"
```

When you run this command, Hexo will try to find `photo.md` in the `scaffolds` folder and build the post based on it. The following placeholders are available in scaffolds:

**Placeholder** | **Description**
----------------|-----------------
`layout`        | Layout
----------------|-----------------
`title`         | Title
----------------|-----------------
`date`          | File created date
