# Perture for Grok Build

Official Perture connection package for Grok Build. It supplies a Grok plugin manifest, a short usage skill, and a remote MCP server locator. The Grok host completes OAuth authorization; no credentials or customer data are bundled.

The remote endpoint is `https://app.perture.co/mcp`. It is the only network endpoint this package calls. A Perture account is required. Some Brand Page editing tools require an active Pro plan, an explicit user request, and OAuth write permission. Reconnect if an older connection has read-only scopes. Perture's service authorizes each request.

## Install

After the [official Grok Build catalog](https://github.com/xai-org/plugin-marketplace) accepts this plugin, install `perture` from Grok Build's Marketplace tab. Enable the Perture MCP connection and complete the browser sign-in when prompted.

Until then, Grok Build can connect to the same remote MCP service directly:

```sh
grok mcp add --transport http perture https://app.perture.co/mcp
```

Open `/mcps` to authenticate and enable the server. This direct connection does not install the usage skill. Do not commit OAuth tokens to the repository.

## Scope and privacy

The package contains no executable hooks, shell commands, local validators, private brand rules, or request client. Brand data, authorization, and protected behavior remain on Perture infrastructure. The host may use tools only within the permissions returned by the connection.

Read the [Privacy Policy](https://app.perture.co/privacy), [Terms of Service](https://app.perture.co/terms), and [support page](https://app.perture.co/support). The connection package is MIT licensed; the hosted Perture service is governed by its own terms.
