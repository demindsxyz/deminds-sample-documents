# Validation Matrix

| Sample | Format | GitHub URL shape | Expected remote behavior | Expected local behavior | Size class | Status | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| markdown/structured-article.md | Markdown .md | blob/raw file | Accepted and imported | Opens as Markdown and Universal Mind Map | tiny | ready | Synthetic public sample. |
| markdown/knowledge-asset-outline.markdown | Markdown .markdown | blob/raw file | Accepted and imported | Opens as Markdown and Universal Mind Map | tiny | ready | Covers .markdown extension. |
| markdown/plain-text-note.txt | Text .txt | blob/raw file | Accepted and imported | Opens through Markdown/text path | tiny | ready | Current parser treats .txt as Markdown-family input. |
| html/clean-article.html | HTML .html | blob/raw file | Accepted and imported as remote document | Converts to Markdown through HTML path | tiny | ready | Not a Web Article test. |
| docx/synthetic-knowledge-asset.docx | DOCX .docx | blob/raw file | Accepted and imported | Converts to Markdown and preserves raw source | tiny | ready | Synthetic DOCX. |
| mindmap/sample.xmind | XMind .xmind | blob/raw file | Accepted and imported | Opens as Original Mind Map and Universal Mind Map | small | ready | Copied from DEV demo fixture. |
| mindmap/xmind-ja-deminds.xmind | XMind .xmind | blob/raw file | Accepted and imported | Opens as Original Mind Map and Universal Mind Map with non-English text | small | ready | Copied from DEV demo fixture. |
| mindmap/sample.mindnode | MindNode .mindnode | blob/raw file | Accepted and imported | Opens as Original Mind Map and Universal Mind Map | small | ready | Copied from DEV demo fixture. |
| mindmap/sample-directory.mindnode | MindNode directory package | tree directory | Accepted when GitHub tree metadata is supported and package stays within normal target | Opens as a directory-style MindNode package with contents.xml and resources | small | ready | Normal-size directory package, about 1.7 MB. |
| mindmap/sample-large-size.mindnode | MindNode directory package | tree directory | Boundary preflight: reject or require local import when above auto-import target | Local import exercises MindNode parser, resource handling, and performance near the size boundary | large-boundary | ready | Public-safe package, about 19 MB, with 20 files and image/PDF resources. Not a first-run sample. |
| mindmap/sample.mm | FreeMind .mm | blob/raw file | Accepted and imported | Opens through FreeMind parser | tiny | ready | Synthetic FreeMind XML. |
| mindmap/dev-freemind-sample.mm | FreeMind .mm | blob/raw file | Accepted and imported | Opens through FreeMind parser with richer styling and notes | tiny | ready | Copied from DEV demo fixture. |
| mindmap/sample.opml | OPML .opml | blob/raw file | Do not present as supported | Not confirmed in local parser/file-open path | none | skipped | remoteDocument mentions .opml, but isSupportedInputName and detectParserType do not. |
| packages/markdown-package-basic.zip | Markdown Package .zip | blob/raw file | Accepted if package size is within archive limit | Opens if supported payload is selected/resolved | tiny | ready | Synthetic Markdown package. |
| packages/markdown-package-with-assets.zip | Markdown Package .zip | blob/raw file | Accepted if package size is within archive limit | Opens Markdown with related asset when supported | tiny | ready | Synthetic package with SVG asset. |
| packages/obsidian-sample-package.zip | Obsidian-style Markdown Package .zip | blob/raw file | Accepted if package size is within archive limit | Opens Markdown notes with related image assets when supported | tiny | ready | Copied from DEV demo fixture; contains Markdown and PNG assets. |
| packages/deminds-backup-sample.zip | DeMinds Workspace Backup .zip | blob/raw file | Deferred | Deferred | none | needs-binary-fixture | Existing DEV demo backup is not used in v0.1 due size/source-noise concerns. |
| Too-large file behavior | Boundary | manual/mock plus sample-large-size.mindnode | Reject above auto-import limit and suggest local import | Local import can still be tried by user | boundary | ready | Covered by the explicit larger MindNode package plus manual/mock cases above the hard limit. |
| Unknown-size generic URL behavior | Boundary | generic URL | Do not silently download | User can download locally | boundary | deferred | GitHub remains the documented first remote path. |
| Git LFS pointer behavior | Boundary | blob/raw file | Detect pointer and avoid treating pointer text as the real payload | User should download actual file if needed | boundary | deferred | Manual validation item for now. |
