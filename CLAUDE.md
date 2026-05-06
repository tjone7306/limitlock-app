# limitlock-app

Native iOS app — open the `.xcodeproj` or `.xcworkspace` file in Xcode.
Companion to `limitlock.pro` (web app, separate repo).

## Xcode-specific notes

- **Apple ID signing:** Xcode → Settings → Accounts. Both Tim's Macs need to
  be signed in with the same Apple ID for provisioning profiles to sync. If
  builds fail with "no eligible signing identity," that's the first thing to
  check.
- **CocoaPods (if used):** after a fresh clone on a new Mac, run
  `pod install` once in this folder. `Podfile.lock` is committed; pod install
  recreates `Pods/` (which is gitignored).
- **Swift Package Manager:** Xcode auto-resolves on first open — no action
  needed.
- **Project.pbxproj noise:** Xcode rewrites this on save even for trivial
  state changes. GitHub Desktop will surface those as changes. Commit them
  with a "xcode auto-format" message — harmless.
- **Don't touch `xcuserdata/` or `DerivedData/`.** Both should be gitignored.

## Workflow

Standard: project lives at `~/dev/limitlock-app/`, GitHub is source of truth
via GitHub Desktop, Claude handles git pull/push transparently.

## Cross-Mac context

`~/Library/Mobile Documents/com~apple~CloudDocs/B4U-Shared/Claude-Context/CONTEXT.md`
has the full project portfolio and Tim's working preferences.
