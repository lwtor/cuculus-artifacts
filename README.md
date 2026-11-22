# cuculus-artifacts

Shared **public** APK artifact repository for the Cuculus update family.

Apps using `cuculus-update` with `UpdateSourceMode.ARTIFACT_REPO` read this repository anonymously. Each app is isolated by a tag prefix (namespace):

```
<namespace>/v<version>    e.g.  cuculus-update/v1.3.5
```

The newest published (non-draft, non-prerelease) release whose tag starts with `<namespace>/` is selected. The APK asset name should end with `-<versionCode>.apk` so the default `AssetNameSuffix()` resolver can read it.

## Entries

| namespace | app | latest |
|---|---|---|
| `cuculus-update` | Cuculus Update demo | `cuculus-update/v1.3.5` |

## Publishing

Releases are created by CI. Do **not** put tokens in any client app — creating releases is a write operation, done only on the publish side via `ArtifactRepoProvisioner` / `softprops/action-gh-release`.
