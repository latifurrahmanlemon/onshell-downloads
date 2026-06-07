# OnShell — Downloads

Public releases of the **OnShell** desktop app (macOS, Windows, Linux).

➡️ **Get the latest installer:** https://github.com/latifurrahmanlemon/onshell-downloads/releases/latest

The OnShell source code lives in a separate private repository.

## Opening OnShell on macOS

OnShell is currently distributed outside the Mac App Store and is not yet
notarized by Apple, so macOS Gatekeeper will block it the first time you try
to open it. This is expected — you only need to allow it once.

### Option 1 — Allow via System Settings (recommended)

1. Double-click **OnShell** once. macOS will show a warning and block it.
   Click **Cancel** or **Done** — **do not** move it to the Trash.
2. Open **System Settings → Privacy & Security**.
3. Scroll down to the **Security** section. You'll see a message such as
   *"OnShell was blocked to protect your Mac."* Click **Open Anyway** next to it.
4. Confirm with **Touch ID** or your password, then click **Open** again.
5. OnShell will now launch normally, and you won't be prompted again.

### Option 2 — Allow via Terminal

If you prefer the command line, remove the quarantine attribute and open the app:

```bash
xattr -dr com.apple.quarantine /Applications/OnShell.app
open /Applications/OnShell.app
```

> Adjust the path if you installed OnShell somewhere other than `/Applications`.

### Why does this happen?

macOS only opens apps from the App Store or from identified, notarized
developers without warning. Until OnShell is signed and notarized, macOS
flags it as coming from an "unidentified developer." The steps above are the
standard, safe way to run such apps and don't lower your Mac's overall security.
