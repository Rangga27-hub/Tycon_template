# BACKEND

> [AI-GENERATED if the type has a backend] Server implementation rules.
> Applies to: web-app, api-service, mobile-app (its backend). Skip for static/ML-only.

## Structure
_(routes → services → data. Where each lives.)_

## Rules
- Separate HTTP layer (routes) from business logic (services) from data access.
- Validate all I/O at the boundary.
- Server-only secrets never leak to client.
- Errors return the standard shape (see API.md); never leak stack traces to clients.

## Services / Modules
| Service | Responsibility | Location |
|---------|----------------|----------|
| _(AI fills)_ | | |

## Background / Async
_(jobs, queues, webhooks, cron — if any.)_

## Testing
_(what gets unit vs integration tested; how to run.)_
