# Size Guidelines

Use small files for remote import testing. Large files should be downloaded locally first and opened from Files or local import.

| Family | Auto import target | Suggest local import above |
| --- | ---: | ---: |
| Text files | 10 MB | 20 MB |
| HTML / DOCX | 10 MB | 20 MB |
| Mind map files | 15 MB | 30 MB |
| Packages | 20 MB | 50 MB |

For package-like files, DeMinds may also check expanded size, file count, large resources, and processing time before completing import.

Keep public samples much smaller than the limits unless a boundary test is explicitly needed.

## Normal-size directory package sample

`mindmap/sample-directory.mindnode` is the small directory-style MindNode package for ordinary tree URL checks. It is about 1.7 MB and includes `contents.xml`, QuickLook preview data, and a few resources.

## Boundary-size sample

`mindmap/sample-large-size.mindnode` is the explicit larger MindNode package for DeMinds size-boundary testing. It is about 19 MB, contains 20 files, and includes several image/PDF resources, with the largest image around 10 MB.

Use it to verify guarded remote behavior, package resource accounting, local import fallback, and parser/performance handling near the mind map size boundary. Do not present it as an onboarding or first-run sample.
