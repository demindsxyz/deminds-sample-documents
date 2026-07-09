# DeMinds Sample Documents

This repository provides mostly small public sample files for DeMinds import testing, Guides, support material, GitHub remote document import smoke checks, and explicit boundary-size checks.

DeMinds is a local-first Markdown + mind map workspace for turning scattered content into maintainable knowledge assets.

## What this repository is for

- Stable public files for trying DeMinds-supported imports.
- GitHub file links for remote import smoke testing.
- Small examples for Guides, release QA, support pages, and demos.
- Explicitly named boundary samples for file type recognition, size checks, guarded download, resource handling, and handoff into the normal DeMinds import flow.

## What this repository is not

- It is not the DeMinds app source repository.
- It is not the DeMinds product website.
- It is not a full documentation site.
- It is not a place for large, private, copyrighted, or confusing fixtures unless a larger public-safe file is explicitly documented as a boundary test.
- It does not advertise unsupported future formats.

## Try a GitHub file link in DeMinds

1. Open a sample file on GitHub.
2. Copy the file page URL or the raw file URL.
3. In DeMinds, choose **Import Web or File Link...**.
4. Paste the link and start the import.
5. DeMinds checks the file size, downloads the file when it is safe to do so, and opens it through the normal local import path.

GitHub is the recommended first remote source because file metadata can usually confirm size before download. For large files, download the file locally first and open it from Files or local import.

## Recommended first samples

- [Structured Article](markdown/structured-article.md)
- [Plain Text Note](markdown/plain-text-note.txt)
- [Clean HTML Article](html/clean-article.html)
- [Structured Report DOCX](docx/structured-report.docx)
- [Sample XMind Map](mindmap/sample.xmind)
- [Sample FreeMind Map](mindmap/sample.mm)

## Supported format overview

Current v0.1 samples cover Markdown, text, HTML, DOCX, XMind, MindNode, MindNode directory packages, FreeMind, and Markdown package zip files. OPML is not represented because the current parser entry point does not list OPML as a supported local input.

## Boundary samples

- [Large MindNode Package](mindmap/sample-large-size.mindnode) is a public-safe MindNode directory package for DeMinds boundary-size and resource-handling checks. It is not a recommended first remote sample.

See [supported formats](docs/supported-formats.md), [GitHub import notes](docs/import-from-github.md), and [size guidelines](docs/size-guidelines.md) for details.

## Privacy note

DeMinds works local-first. These public samples are safe to download and test, but your own documents should stay under your control. Use local import for private files or large files.
