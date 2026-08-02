# R-Zero

R-Zero Systems is a San Francisco based building-intelligence company founded in 2020 that combines
privacy-first occupancy sensors, indoor-air-quality monitoring and AI to autonomously optimize HVAC
ventilation in commercial real estate, healthcare and higher-education buildings — claiming 20–40%
HVAC energy savings with no retrofits or capital investment. Its platform, R-Zero Connect, turns raw
sensor telemetry into occupancy analytics, space-utilization insights and portfolio reporting.

R-Zero's developer surface comes from **CoWorkr**, the workplace-sensor company it acquired:

- **CoWorkr REST API** — pull historical and current workplace utilization data into BI tooling.
- **CoWorkr Stream API** — Node.js/DDP push of real-time occupancy events into reservation and
  workplace-experience applications (AgilQuest, Comfy, iOffice Hummingbird, Serraview, Teem).

Both APIs are **account-gated**: the reference is served inside the authenticated CoWorkr application
and access is granted per account on request to R-Zero support. No public OpenAPI, GraphQL, MCP or
A2A surface is published — see `well-known/r-zero-well-known.yml` for the full contract-discovery
record.

## Artifacts

| Path | What it holds |
|---|---|
| `data-model/` | The CoWorkr object model (WorkPoint, Counter, WorkHub, WorkPlace, FloorPlan, Tag) from R-Zero's published API Definitions |
| `vocabulary/` | Device, platform, analytics and API terms as R-Zero defines them |
| `conventions/` | Access model, UTC timestamp format, identifier shapes, tagging and active-hours semantics |
| `conformance/` | SOC 2 Type II / SOC 3 posture and the standards R-Zero does not claim |
| `lifecycle/` | Status page, hardware generations, and the absence of a versioning/deprecation policy |
| `security/` | Domain security probe + trust-center capture |
| `packages/` | Registry search result — no first-party SDKs published |
| `well-known/` | `/.well-known/` probe and full contract-discovery record |
| `llms/` | Generated llms.txt |

- https://rzero.com/
- https://coworkr.co/apiaccess
- https://forgeglobal.com/r-zero_stock/
