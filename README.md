# repo

Personal iOS jailbreak APT repository hosted with GitHub Pages.

Repo URL after GitHub Pages is enabled:

```text
https://reloadline.github.io/repo/
```

Add it in a package manager:

- Sileo: `sileo://source/https://reloadline.github.io/repo/`
- Zebra: `zbra://sources/add/https://reloadline.github.io/repo/`
- Cydia: `cydia://url/https://cydia.saurik.com/api/share#?source=https://reloadline.github.io/repo/`

## Add packages

1. Put your `.deb` files in `插件/`.
2. Rebuild the package indexes:

   ```sh
   dpkg-scanpackages -m 插件 /dev/null > Packages
   gzip -n -c Packages > Packages.gz
   bzip2 -c Packages > Packages.bz2
   ```

3. Update `Release` checksums, then commit and push or upload the changed files.

Only publish packages you own or have permission to redistribute. Do not use this repo for cracked apps, malware, or unauthorized content.
