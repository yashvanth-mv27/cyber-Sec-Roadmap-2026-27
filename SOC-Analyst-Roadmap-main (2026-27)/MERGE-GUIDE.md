# Non-destructive integration guide

The existing GitHub repository must remain unchanged until a reviewed PR is merged.

1. Obtain GitHub App **Contents: read/write** permission and permission to create refs/branches (Git data).
2. Create a feature branch from current main.
3. Add the `advanced/`, `assets/`, and `diagrams/` files without deleting any existing paths.
4. Append README-ADVANCED-2027.md to the existing README.md, rather than overwriting it.
5. Open a PR, review Markdown links and Mermaid diagrams, then merge only after approval.

The previous expansion's `modules/` folder and README-ENHANCEMENT.md are included as an additive proposal. No repository files were modified by this package.
