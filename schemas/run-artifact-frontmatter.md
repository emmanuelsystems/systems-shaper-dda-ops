# Run Artifact Frontmatter

Status: `candidate_review_only`

Use this frontmatter shape for dated run artifacts when a structured header is useful.

```yaml
---
title:
date:
status: draft | candidate | review-ready | accepted | held | rework | rejected
artifact_type:
source_index:
branch:
commit:
reviewer:
proof_boundary:
non_claims:
---
```

## Boundary

Frontmatter improves consistency. It does not create acceptance or validation.
