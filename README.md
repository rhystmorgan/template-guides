# Template Guides

This repo is a template for Codio lessons,

It is not a replacement for whole courses or even modules it can only work for individual lessons.

---

## How To Use This Template

This template is designed for writing course material for codio outside of the platform so it can easily be managed, updated and edited.

The course content is in `.guides` and within that you have subdirs for content, chapters, sections and pages.

Each chapter/section has its own dir and within that there is an `index.json` which details the name and the order of subdirs/content.

You can start with what is provided and duplicate them out as needed instead of rewriting everything from scratch as there is a lot of boilerplate json that we dont need to edit.

### Pages 

Pages have the actual course material, they are comprised of 2 files, a `.md` file with the content & a `.json` file with the page metadata.

You nede both of these.

If you want to have pages with the same name, you can make the `title` field in the json the same, but the file names need to be unique, so add numbers or a string to the file names

eg:

Page 1 - Introduction
  - intro1.md
  - intro1.json
    - title: Introduction

Page 2 - Introduction
  - intro2.md
  - intro2.json
    - title: Introduction

```json
{
  ...
  "title": "Introduction",
  ...
}
```

These will both be titled `Introduction` in codio on the actual page, but you can order them in the root `index.json` to ensure they are ordered correctly

```json
{
  "id": "",
  "type": "section",
  "title": "Section Title",
  "order": [
    "intro1",
    "intro2"
  ]
}
```

