# Software Development Workflow

## Phase Flow

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│  Requirement│    │ Architecture│    │    Design   │    │ Development │    │    Review   │
│    Issue    │───▶│   Design    │───▶│   Details   │───▶│  + Code PR  │───▶│ + All Agents│──▶ Done
└─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘
       │                  │                  │                  │                  │
       │                  │                  │                  │                  │
       ▼                  ▼                  ▼                  ▼                  ▼
  [User Creates]    Architect drafts    Designer creates    Developer codes    Multi-Agent
                     User LGTM ▲       User LGTM ▲         Tester tests      Review
                                │                  │                  │
                                └──────────────────┴──────────────────┘
                                            LGTM Required
```

## Multi-Agent Code Review

When development is ready, ALL agents participate in code review:

| Agent | Review Focus |
|-------|--------------|
| **architect** | Architecture compliance, technology choices |
| **designer** | Design completeness, interface standards |
| **developer** | Code quality, best practices |
| **tester** | Test coverage, edge cases, bug risks |

After all agents approve → User final LGTM → Done

## Issue Labels

| Label | Phase | Description |
|-------|-------|-------------|
| `requirement` | 0 | New requirement submitted |
| `architecture` | 1 | Architecture design phase |
| `design` | 2 | Detailed design phase |
| `development` | 3 | Code implementation phase |
| `review` | 4 | Multi-agent code review |
| `pending-lgtm` | * | Awaiting user approval |
| `approved` | * | Approved, proceed to next phase |
| `rejected` | * | Rejected, needs rework |

## Approval Process

1. Agent creates/updates issue with phase deliverable
2. Agent sets `pending-lgtm` label
3. User reviews and comments `LGTM` or `NACK`
4. If LGTM: User changes label to `approved`, agent proceeds
5. If NACK: User comments issues, agent fixes and resubmits

## GitHub Issue Templates

- **Requirement**: For submitting new requirements
- **Architecture**: For architecture design documents  
- **Design**: For detailed design documents

## Agent Assignment

| Issue Label | Assigned Agent |
|-------------|----------------|
| `requirement` | main (PM) |
| `architecture` | architect |
| `design` | designer |
| `development` | developer |
| `review` | architect + designer + developer + tester |
