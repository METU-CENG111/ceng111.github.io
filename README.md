# CENG 111 website

Source for <https://ceng111.github.io>. Built automatically by GitHub Pages (Jekyll) —
there is nothing to install and nothing to build on your computer.

## Putting it online (once)

1. Create a GitHub organisation or user account named **`ceng111`**.
2. Under it, create a public repository named **`ceng111.github.io`**.
3. Drag and drop *the contents of this folder* (not the folder itself) into the repo
   through the browser, and commit.
4. Repo **Settings → Pages → Build and deployment**: source *Deploy from a branch*,
   branch `main`, folder `/ (root)`.
5. Wait ~1 minute, then open <https://ceng111.github.io>.

Every later commit rebuilds the site automatically, usually within a minute.

## Editing content

Each tab is one Markdown file in the repo root:

| Tab | File |
|---|---|
| Home | `index.md` |
| Course Info | `course.md` |
| Schedule | `schedule.md` |
| Lab | `lab.md` |
| Exams & Grading | `exams.md` |
| Resources | `resources.md` |

To change text: open the file on GitHub, click the pencil icon, edit, then
**Commit changes**. Markdown basics are all you need:

```markdown
## A heading

Normal text. **Bold.** *Italic.* A [link](https://example.com).

- a bullet
- another bullet

| Column | Column |
|---|---|
| cell   | cell   |
```

Leave the block at the very top of each file (between the `---` lines) alone —
that is what tells GitHub Pages which tab the file is.

Lines that look like `<!-- ... -->` are notes to you; they never appear on the site.

## Adding or renaming a tab

Edit `_config.yml`, in the `nav:` list. To add a tab, add two lines there **and**
create a matching `.md` file whose `permalink:` is the same as the `url:` you used.

## Uploading PDFs and other files

Drop them into the `files/` folder and link to them from a page:

```markdown
[Lab Manual (PDF)]({{ '/files/lab_manual.pdf' | relative_url }})
```

See `files/README.md` for the files the pages currently expect.

## Changing the design

`assets/css/style.css` holds all the styling, `_layouts/default.html` the page frame.
You do not need to touch either one to update course content.
