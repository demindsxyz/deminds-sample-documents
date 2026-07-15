# File Size Thresholds

Current user-facing guidance:

| Family | Auto import target | Suggest local import above |
| --- | ---: | ---: |
| Text files | 10 MB | 20 MB |
| HTML / DOCX | 10 MB | 20 MB |
| Mind map files | 15 MB | 30 MB |
| Packages | 20 MB | 50 MB |

Maintainer guard summary:

- Stop if downloaded size exceeds expected size + 10%.
- Stop if extracted size is more than 8-10x the outer file size.
- Stop if extracted total size exceeds 100 MB.
- Stop or warn if file count exceeds 2,000.
- Skip or warn for a single image resource above 20 MB.
- Stop parsing after 20-30 seconds and suggest local import.

Boundary-size sample:

- `mindmap/sample-large-size.mindnode` is about 19 MB and should be used for guarded MindNode package checks near the mind map auto-import boundary.

Normal-size directory package sample:

- `mindmap/sample-directory.mindnode` is about 812 KB and should be used when validating ordinary GitHub tree import for directory-style MindNode packages.
