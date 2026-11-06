# scoop-bucket

This repository holds the [Scoop](https://scoop.sh) bucket for [Aggrega](https://aggrega.ai): the manifest that installs the `aggrega` binary on Windows.

## Install

Add the bucket once, then install from it:

```powershell
scoop bucket add aggrega https://github.com/aggrega-ai/scoop-bucket
scoop install aggrega
```

Scoop installs the binary for Windows on 64-bit x86 as `aggrega.exe`, downloaded from the Aggrega release on GitHub and checked against the SHA-256 digest the manifest gives it, and makes it reachable as `aggrega` through the folder of shims it keeps on your `PATH`. After a new release, `scoop update` refreshes the buckets and `scoop update aggrega` updates it.

Scoop installs into its own folders, and updates only the copy it installed. Use one way of installing Aggrega on a machine: [Install](https://aggrega.ai/docs/install/#install-with-a-package-manager) describes the others.

## Where these files come from

`bucket/aggrega.json` is written by every Aggrega release, from a template in [aggrega-ai/aggrega-cli](https://github.com/aggrega-ai/aggrega-cli), and names that release's binary and its digest. Do not edit it by hand: the next release replaces it. A change to the manifest is made to the template there.

## License

The Aggrega Scoop bucket is released under the Apache License, Version 2.0; the full text is in the [`LICENSE`](LICENSE) file.
