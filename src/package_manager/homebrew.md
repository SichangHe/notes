<!-- toc -->
# Homebrew

search package

```shell
brew search <package>
```

install package

```shell
brew install <package>
```

update

```shell
brew update \
&& brew upgrade --greedy \
&& brew cleanup \
&& brew autoremove
```

list installed packages

```shell
brew list
```

show dependency tree of package

```shell
brew deps -t <package>
```

display information about package

```shell
brew info <package>
```

clean up junk

```shell
brew cleanup && brew autoremove
```
