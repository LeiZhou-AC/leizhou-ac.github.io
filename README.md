# Lei Zhou Personal Homepage

This is the editable local working copy for `https://leizhou-ac.github.io/`.
It is a Jekyll site based on AcademicPages / Minimal Mistakes and is deployed by
GitHub Pages from the `LeiZhou-AC/LeiZhou-AC.github.io` repository.

## Local Development

Install dependencies:

```bash
./bin/bootstrap
```

Start the local preview server:

```bash
./bin/serve
```

The scripts force a UTF-8 locale so Chinese text in page titles and body content
builds correctly under the macOS system Ruby.

For a quiet background server, disable LiveReload:

```bash
DETACH=1 LIVERELOAD=0 ./bin/serve
```

If the detached Jekyll server exits on the macOS system Ruby, build once and
serve the generated `_site` directory:

```bash
./bin/static
```

Then open:

```text
http://127.0.0.1:4000/
```

If `bundle install` hangs while contacting RubyGems, retry on a stable network or
use a mirror:

```bash
RUBYGEMS_MIRROR=https://gems.ruby-china.com ./bin/bootstrap
```

## Main Edit Points

- Home page: `_pages/about.md`
- Site title, URL, author profile, avatar, email, social links: `_config.yml`
- Top navigation: `_data/navigation.yml`
- Publications page shell: `_pages/publications.md`
- CV page: `_pages/cv.md`
- Uploaded PDFs or attachments: `files/`
- Images and avatar: `images/`

Detailed add/edit/delete/search instructions are in `docs/content-guide.md`.
