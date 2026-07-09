# Expected Behavior

A supported GitHub file link should be checked before download, downloaded only when it is within the remote limit, and then handed to DeMinds' normal local import pipeline.

| Case | Expected behavior |
| --- | --- |
| Supported small file | Accepted and imported. |
| Supported file over auto limit | Rejected with guidance to download locally first. |
| Unknown-size file | Not silently downloaded. |
| Unsupported extension | Rejected before download. |
| GitHub folder | Rejected unless it is a supported MindNode package directory path. |
| Web article URL | Handled by Web Article / Web Import Preview, not this remote document path. |
