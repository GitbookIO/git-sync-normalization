---
description: All content blocks and how we translate them to markdown
---

# Git Sync

When GitBook exports one of your spaces to a GitHub repository, it translates all content to markdown. GitBook is opinionated. If there are different ways to express the same concept or style in markdown, GitBook will only use one.

For example, in markdown you can have an unordered list start with a `-` or a `*`. Both are valid characters for a bullet list. GitBook, however, will always default to `*`.

If your repository has markdown content that uses `-`, GitBook will change that to `*` during the synchronization that happens from GitBook to GitHub.

If you add new content or change existing content to use markup that's not GitBook's flavor, GitBook will change it back at the next opportunity.

This space has examples of all content blocks and how those are translated as markdown content.

This is the repository this space is synched with:

{% embed url="https://github.com/GitbookIO/git-sync-normalization" %}



