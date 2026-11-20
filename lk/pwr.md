---
name: "es-readonly"
displayName: "Elasticsearch Read-Only Query Assistant"
description: "Query Elasticsearch and Kibana — search logs, run aggregations, check cluster health, and explore indices via a read-only MCP server"
keywords: ["elasticsearch", "kibana", "es", "logs", "search", "aggregation", "cluster", "index", "mapping", "query"]
---

# Onboarding

## Step 1: Validate MCP server is accessible
Verify the ES MCP server is running by checking cluster health:
- Use the `es_query` tool with path `/_cluster/health`
- If it fails, ensure the MCP server is configured and credentials are valid

## Step 2: Understand available tools
This power provides two tools:
- `es_query` — GET requests (cluster health, index listings, mappings, settings, ILM policies)
- `es_post` — POST requests to read-only endpoints only (_search, _count, _msearch, _field_caps)

Use `es_post` for aggregations and complex queries that need a JSON body.

# When to Load Steering Files
- Searching logs or querying documents → `query-patterns.md`
- Checking cluster health, nodes, or indices → `cluster-ops.md`
