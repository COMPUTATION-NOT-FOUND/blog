# Contributing

Practical guidelines for writing and reviewing posts. See [README.md](README.md) for the mechanics of adding a post.

## Why forks

Writers contribute from their own fork rather than a branch on this repo. That keeps push access to this repo scoped to maintainers only, and keeps this repo's branch list from filling up with one branch per post. Open your PR from your fork's branch into this repo's `main`.

## Writing style

- Write for someone who knows CS fundamentals but not the specific system you're covering. Explain the "why" behind a design decision, not just the "what."
- Prefer concrete detail over generic statements. "Reduced page-fault latency from 40µs to 12µs by batching TLB shootdowns" beats "improved performance."
- Keep code blocks minimal and runnable/representative. Trim anything that doesn't support the point being made.
- It's fine to write about work that isn't finished (`status: draft`) or didn't pan out. A clearly-explained dead end is still useful.

## Before opening a PR

- **Frontmatter is complete and accurate.** `excerpt` in particular: it's what shows up on the blog index and as the page's meta description, so make it count rather than leaving it as a placeholder sentence.
- **`category`/`tags` match how the rest of the blog is organized.** Skim a couple of existing posts rather than inventing a new category for a one-off.
- **Images are `.webp`, reasonably sized**, and have real alt text (not the filename).
- **`author` is your actual slug.** If you don't have one yet, ask a maintainer. Don't merge a post under someone else's name or a placeholder.
- **Proofread.** CI checks structure (frontmatter fields, image format), not writing quality. That's the reviewer's job, and yours before you ask for review.

## Review expectations

A reviewer is checking for:

- Technical accuracy: does the post actually describe what the system does?
- Nothing that misrepresents another contributor's work or attributes it incorrectly.
- Reasonable length and focus. A post that tries to cover everything usually explains nothing well.
- No raw HTML beyond what's actually needed (frontmatter allows it, but Markdown should be the default).

Small wording suggestions can happen directly on the PR; anything structural (scope, accuracy, missing context) is worth a comment before approving.

## Commits

Commit messages: plain description of what changed (`Add post: RISC-V Cache Coherency`, `Fix broken link in intro`), no need for a strict format. Keep post-content changes and unrelated fixes (typo in another post, README tweak) in separate PRs where reasonable, so review stays focused.
