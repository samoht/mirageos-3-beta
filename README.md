This repository is a staging repository for the set of libraries that are referenced by MirageOS 3.  The easiest way to use it is to add the repository as a package remote in `opam`:

```
opam remote add mirage-3 https://github.com/mirage/mirageos-3-beta.git
opam update
```

Please note that remotes are global in `opam`, so once you have executed the commands above, any `opam upgrade` or `opam install` will consider the set of packages in this repository as fair game regardless of the active switch.  If you wish to keep a switch on the current stable MirageOS release, pin the versions of `mirage-types` and `mirage` in that switch:

```
opam switch mirageos-version-2
opam pin add mirage-types 2.8.0
opam pin add mirage 2.9.1
```

The constraints on the package universe in `opam-repository` and `mirage-3` *should* prevent conflicts if you pin mirage-types and mirage to pre-3 versions.  If you get surprising results, please let us know.
