---
opener: minor
opener-js: minor
---

On Linux and the BSDs, updated `zbus` to version 6. The `zvariant`, `zbus_names` and `zvariant_derive` crates, which RustSec flags as unmaintained (RUSTSEC-2026-0370, RUSTSEC-2026-0371 and RUSTSEC-2026-0372), are no longer in the plugin's dependency tree. The public `Error::Zbus` variant wraps `zbus::Error`; applications using this type directly should update their `zbus` dependency. A session bus address with the `unixexec:` transport now needs zbus's `unixexec` feature, which the plugin does not enable.
