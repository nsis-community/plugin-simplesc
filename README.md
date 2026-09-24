# build-plugin-simplesc

Test fixture for [nsis-dev/build-plugin](https://github.com/nsis-dev/build-plugin).

> [!CAUTION]
> This is not an official plugin repository.

**Covers:** The common Pascal case. A Delphi `.dpr` with two more units, calling Windows service and LSA APIs.

**Changed from upstream:** Dropped the bundled ANSI-only `NSIS.pas` so the one NSIS ships is used; export signatures `variables: PChar` became `variables: NSISPTChar` so unicode targets type-check. For Free Pascal, under `{$IFDEF FPC}`: `JwaWinSvc` instead of `WinSvc`, `GetLastError` instead of `System.GetLastError`, a pointer to `EnumDependentServices`, and `$00010000` for `DELETE`.
