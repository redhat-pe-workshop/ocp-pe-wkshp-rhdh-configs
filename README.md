# RHDH Config Progression

Kustomize overlays for the Platform Engineer workshop track. Each overlay builds on the previous, progressively configuring Red Hat Developer Hub from a minimal deployment to a fully-featured IDP.

Attendees advance through stages by updating their Argo CD Application's `spec.source.path`.

## Structure

| Path | Stage |
|------|-------|
| `base/` | Minimal RHDH with guest auth |
| `overlays/02-sso-plugins/` | SSO, integrations, and dynamic plugins |
| `overlays/03-catalog-entities/` | Software catalog populated with Parasol entities |
| `overlays/04-templates/` | Golden-path software templates and RBAC |
| `overlays/05-lightspeed/` | AI assistant with Lightspeed and MCP |

## Cluster values

Files use `{{ cluster_subdomain }}` and `{{ kubernetes_api_url }}` Jinja2 placeholders, substituted by the provisioning automation at deploy time.
