# PKG Team Plugins

## PK.Game Month Theme Studio

Version 1.0.1. Contains one artwork skill plus three style references. No MCP servers, hooks, API keys, or external service configuration are bundled. Image generation uses the capability available in the operator's Codex environment.

## Workspace distribution

PKG admin: Admin > Plugins > Add > Import marketplace. Source: https://github.com/rafaelxu84/pkgame-team-plugins. Path: empty. Ref: main. Review import results and set the plugin installation policy to Available for intended members.

## Local Codex marketplace

```sh
codex plugin marketplace add rafaelxu84/pkgame-team-plugins --ref main
```

Private-repository access is required for direct Git-based installation. Workspace import uses the importing admin's GitHub connection. Open the client Plugins directory, select PKG Team Plugins, and install PK.Game Month Theme Studio. Start a new chat and invoke `$pkgame-month-theme-studio`. Exact client availability must be verified; a workspace import alone is not proof of desktop installation.

## Monthly updates

Edit `plugins/pkgame-month-theme-studio/skills/pkgame-month-theme-studio/references/current-theme.json` and replace reference images only when a new shared theme is approved. Preserve operator-controlled scope. Increment both plugin manifests and skill metadata versions together. Commit to main, then request Sync now in Admin > Plugins > Marketplaces. Verify import status and the version available to clients. Do not promise immediate automatic local updates.

## Brief example

Use PK.Game Month Theme Studio. Create an image, 2.13:1, width 1280px, with a football and boots. Use the current theme, no text or logo.
