<!-- toc -->
# Nix

find package: search online

install prebuilt package

```shell
nix-env -ibA <PACKAGE>
```

install package

```shell
nix-env -iA <PACKAGE>
```

update all nix package

```shell
nix-channel --update && nix-env -u
```

check and fix nix store

```shell
sudo nix-store --verify
```
