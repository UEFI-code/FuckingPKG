# FuckingPKG

U know, install a pkg need Admin privilege...And it may contains fucking scripts that polluting your Mac.

So, try NOT double-click a pkg. Expand it instead.
```bash
pkgutil --expand install.pkg install_pkg
cd install_pkg
cat Payload | cpio -idm
```

If cpio failec, try
```bash
gzip -dc Payload | cpio -idm
```
