# Chronary OpenAPI

The official OpenAPI 3.1 specification and Postman collection for the [Chronary](https://chronary.ai) calendar-as-a-service API.

This repository is a published snapshot of the spec, regenerated on every public release of the Chronary API.

## What's in here

- `openapi.json` — OpenAPI 3.1 specification for the Chronary REST API. Auto-generated from the API source in the private Chronary monorepo on each release.

## Using the spec

### Import into Postman / Insomnia

Most API tools can import an OpenAPI 3.1 document directly:

```bash
curl -O https://raw.githubusercontent.com/Chronary/chronary-openapi/main/openapi.json
```

Then import `openapi.json` in Postman → Import → File.

### Generate clients

Use [openapi-generator](https://openapi-generator.tech/) or [oapi-codegen](https://github.com/oapi-codegen/oapi-codegen) to generate clients in your language of choice:

```bash
openapi-generator-cli generate \
  -i https://raw.githubusercontent.com/Chronary/chronary-openapi/main/openapi.json \
  -g typescript-axios \
  -o ./chronary-client
```

> Chronary maintains official SDKs for [TypeScript](https://github.com/Chronary/chronary-node), [Python](https://github.com/Chronary/chronary-python), and [Go](https://github.com/Chronary/chronary-go). For Claude Desktop, Cursor, VS Code, and Windsurf, see [chronary-mcp](https://github.com/Chronary/chronary-mcp).

### Browse interactively

Paste the raw URL above into [Swagger Editor](https://editor.swagger.io/), [Stoplight Studio](https://stoplight.io/studio), or any OpenAPI viewer.

## Versioning

This spec mirrors the live API at [api.chronary.ai](https://api.chronary.ai). The Chronary API is versioned under `/v1/`; the spec is updated atomically when the API is updated.

## Related repositories

| Repository | Purpose |
| --- | --- |
| [chronary-node](https://github.com/Chronary/chronary-node) | TypeScript SDK (`@chronary/sdk`) |
| [chronary-python](https://github.com/Chronary/chronary-python) | Python SDK (`chronary`) |
| [chronary-go](https://github.com/Chronary/chronary-go) | Go SDK |
| [chronary-mcp](https://github.com/Chronary/chronary-mcp) | MCP server for AI IDEs |
| [chronary-cli](https://github.com/Chronary/chronary-cli) | Command-line tool |

## License

Apache-2.0. See [LICENSE](LICENSE) (if present in this repository) or the [Chronary terms of service](https://chronary.ai/terms).
