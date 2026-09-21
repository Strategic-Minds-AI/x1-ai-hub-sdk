# x1-ai-hub-sdk

**Strategic Minds AI — X1 AI Hub OS**

> **Role**: Public-facing TypeScript/Python SDKs, host adapters, examples, quickstarts and developer growth surface.

---

## Authority
Developer experience and client integration authority. Canonical library for external developers and host applications integrating with X1 AI Hub.

Canonical repository: `Strategic-Minds-AI/x1-ai-hub-sdk`  
Default branch: `main`  
Bootstrap branch: `bootstrap/x1-ai-hub-os-v1`  
Production release status: **LOCKED** (`production_release: LOCKED`)  
Visibility: **PUBLIC**

---

## Responsibilities
- Maintain ergonomic TypeScript (`@x1-ai-hub/sdk`) and Python (`x1-ai-hub-sdk`) client packages.
- Provide framework host adapters (Node.js, Next.js, FastAPI, LangChain, LlamaIndex).
- Publish runnable developer quickstarts, code examples, and interactive tutorials.
- Maintain compatibility matrices across host framework versions.

---

## Non-Responsibilities
- Implementing internal control plane orchestration logic.
- Running backend database infrastructure or raw MCP server handlers directly.

---

## Upstream and Downstream Interfaces

### Upstream Interfaces
- x1-ai-hub-protocol (wire contracts, OpenAPI specs, and TypeScript/Python types)

### Downstream Interfaces
- External developer applications, third-party integrations, and x1-ai-hub frontend

---

## Local Development
Prerequisites: Node.js >= 18, Python 3.11+, pnpm / poetry.
Commands:
```bash
npm install
npm run build # Builds TypeScript and Python SDK artifacts
npm run test  # Runs SDK test suite
```

---

## Tests
SDK unit and mock integration tests (`npm test`). Cross-language API parity tests (`npm run test:parity`). Framework compatibility matrix test suite (`npm run test:compatibility`).

---

## Validation Gates
- 100% pass on API compatibility matrix across supported Node.js and Python versions.
- 100% export documentation and declaration coverage.
- Dependency security audit (`npm audit`) clean with zero vulnerabilities.
- CI pipeline gate (`.github/workflows/x1-bootstrap-ci.yml`) must pass.

---

## Security
Zero runtime dependencies with known vulnerabilities. API keys transmitted strictly via encrypted TLS authorization headers; credentials never cached to disk.

---

## Deployment
Published to public NPM registry (`@x1-ai-hub/sdk`) and PyPI (`x1-ai-hub-sdk`) upon git release tag creation (`v*.*.*`).

---

## Rollback
NPM/PyPI package version deprecation (`npm deprecate`) and rapid patch release issuance.

---

## Receipts
Emits `SdkReleaseReceipt` artifacts containing package SHA-256 integrity hashes, API export signature hashes, and build logs.

---

## Ownership and Handoff
- **Owner**: Strategic Minds AI - Developer Relations & SDK Engineering Team (`Strategic-Minds-AI`)
- **Handoff Contract**: Owned by Strategic Minds AI - Developer Relations & SDK Engineering Team (`Strategic-Minds-AI`). Handoff requires NPM/PyPI publish verification receipt, cross-language parity pass certificate, and operator approval.
- **Operating Contract**: All modifications belong to `bootstrap/x1-ai-hub-os-v1` branch until approved by the operator. Changes to machine contracts require dependency impact analysis, counterpart interface updates, and fresh `VERIFIED_100` evidence verification.
