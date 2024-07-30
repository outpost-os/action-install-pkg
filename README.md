# Multi-platform package installer

## Intro

This action aim to abstract various distro (including OS-X) packagers through a
unified interface, in order to install packages.

As a very same software may be packaged with different names on different distros,
this action support fallback methodology so that it success while any of the
possible names of a package is fully installed

## Usage

Separating possible names for a very same package is done using `|`
Separating different packages is done using `,`

Here is a typical usage:
```
- name: install curl and dts packages
  uses: embedded-devops/action-install-pkg@v2.0
  with:
    packages: 'dtc|device-tree-compiler,curl'
```

