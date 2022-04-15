# Useful terminal commands

## Find and delete node_modules

Test command to find what's going to get deleted and the sizes

```bash
find . -type d -name 'node_modules' -prune | xargs du -chs
```

Do the actual removal

```bash
find . -name "node_modules" -type d -prune -exec rm -rf '{}' +
```
