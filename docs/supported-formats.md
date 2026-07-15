# Supported Formats

This page reflects the current DeMinds DEV source checked for v0.1 of this repository.

## Included in this repository

| Family | Extensions | Samples | Notes |
| --- | --- | --- | --- |
| Markdown / text | .md, .markdown, .txt | markdown/ | The current parser treats .md, .markdown, and .txt as Markdown-family inputs. |
| HTML | .html, .htm | html/ | GitHub file links are documented here as remote document imports. Web Article import is a separate path. |
| DOCX | .docx | docx/ | DOCX imports produce Markdown while preserving the raw source in DeMinds. |
| XMind | .xmind | mindmap/sample.xmind; mindmap/xmind-ja-deminds.xmind | Covered by the mind map parser, including non-English text fixtures. |
| MindNode | .mindnode, .mindnode.zip | mindmap/sample.mindnode; mindmap/sample-directory.mindnode; mindmap/sample-large-size.mindnode | Includes a small file-style sample, a normal-size directory package, and a larger directory package for boundary-size checks. Directory-style .mindnode packages require a main entry such as `contents.xml` or `contents.data`. |
| FreeMind | .mm | mindmap/sample.mm; mindmap/dev-freemind-sample.mm | Covered by the FreeMind parser. |
| Markdown / Obsidian-style packages | .zip | packages/markdown-package-*.zip; packages/obsidian-sample-package.zip | Zip packages are accepted when they contain supported Markdown-family payloads and related assets. |

## Supported by DeMinds but not yet represented in v0.1

| Format | Reason |
| --- | --- |
| DeMinds Workspace Backup zip | Deferred for v0.1 because the available DEV demo backup is larger and contains mixed historical demo material. A smaller public-safe backup should be generated in a later pass. |

## Not currently supported from the checked source

| Format | Status |
| --- | --- |
| OPML (.opml) | Status: unknown from current source pack for local import. The remote document classifier mentions OPML as a mind map kind, but isSupportedInputName(...) and detectParserType(...) do not list .opml. Do not publish OPML as supported until the parser/file-open path is implemented. |
| Generic JSON | Not listed as a supported local import format. |
| Arbitrary GitHub folders | Not supported as a repository browser or recursive import path. |

GitHub remote import is the primary documented remote path for these samples. Generic remote files should not be described as broadly supported unless DeMinds can confirm size before download.
