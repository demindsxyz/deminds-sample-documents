# Troubleshooting

## The link is not a direct GitHub file link

Open the file on GitHub and copy the file page URL or raw URL. Do not paste a repository home page or folder page unless the feature specifically supports that package path.

## The file is too large for remote import

Download it locally first, then open it from Files or local import.

## DeMinds cannot confirm the remote file size

Use a GitHub file link or download the file locally. Unknown-size remote files should not be silently downloaded.

## The file type is unsupported

Check [supported formats](supported-formats.md). Do not rename an unsupported file to a supported extension.

## The file imports locally but not remotely

The remote path may lack reliable size metadata, may be private, or may be rate limited. Download the file and import it locally.

## A GitHub private repository or rate limit blocks access

Use a public file link for samples. Private repositories may require authentication that DeMinds does not ask users to configure for this first public path.

## HTML pages and web articles are different paths

HTML sample files are document files. Web Article import is a separate path for readable article pages.
