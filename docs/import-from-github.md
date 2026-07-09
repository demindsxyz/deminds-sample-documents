# Import from GitHub

GitHub file links are the recommended first remote sample path for DeMinds.

The intended flow is:

```text
GitHub file link
-> size preflight
-> guarded download
-> temporary local file
-> existing DeMinds import pipeline
```

DeMinds does not clone repositories and does not browse an entire GitHub repository. It treats a supported GitHub file link as a remote file that can be checked before download.

## Good URL shapes

- `https://github.com/demindsxyz/deminds-sample-documents/blob/main/markdown/structured-article.md`
- `https://raw.githubusercontent.com/demindsxyz/deminds-sample-documents/main/markdown/structured-article.md`
- `https://github.com/demindsxyz/deminds-sample-documents/blob/main/docx/synthetic-knowledge-asset.docx`

For old-style MindNode directory packages, use that path only when the current DeMinds source supports a GitHub tree URL for a .mindnode directory containing `contents.xml` or `contents.data`.

## What happens after paste

1. DeMinds checks whether the file name is supported.
2. GitHub metadata is used to confirm size when available.
3. Files above the remote auto-import limit are rejected with guidance to download locally first.
4. Accepted files are downloaded and opened through the same import path as local files.

Remote document import is separate from Web Article and Web Import Preview. HTML files in this repository are document samples, not live web article pages.
