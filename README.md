# feedbackiq-demo

Target repository for [FeedbackIQ](https://github.com/NuroArt/feedbackiq). No code lives here by design — the point is the issue tracker.

Every issue in this repo was filed automatically by FeedbackIQ's pipeline from analyzed customer feedback: classified against a strict schema, clustered into themes, ranked by priority score, and filed when the theme crossed the severity threshold. The issue bodies, titles, and representative quotes are all generated output.

The comment threads are the part worth looking at. FeedbackIQ's issue upsert is idempotent — on a re-run it matches existing issues by body marker and theme similarity rather than filing duplicates, so a theme the model re-words between runs still lands on the same issue and gets a comment instead of a second ticket. The threads here are that matching surviving six successive re-wordings against the live GitHub API.
