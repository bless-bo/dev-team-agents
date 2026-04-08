# Software Development Workflow

## Phase Flow

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│  Requirement│    │ Architecture│    │    Design   │    │ Development │    │   Testing   │
│    Issue    │───▶│   Design    │───▶│   Details   │───▶│  + Code PR  │───▶│   Report    │
└─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘
       │                  │                  │                  │                  │
       │                  │                  │                  │                  │
       ▼                  ▼                  ▼                  ▼                  ▼
  [User Creates]    Architect drafts    Designer creates    Developer codes    Tester tests
                     User LGTM ▲         User LGTM ▲         Tester reviews    User LGTM ▲
                                │                  │                  │
                                └──────────────────┴──────────────────┘
                                            LGTM Required
```

## Issue Labels

| Label | Phase | Description |
|-------|-------|-------------|
| `requirement` | 0 | New requirement submitted |
| `architecture` | 1 | Architecture design phase |
| `design` | 2 | Detailed design phase |
| `development` | 3 | Code implementation phase |
| `testing` | 4 | Testing and QA phase |
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
| `testing` | tester |
