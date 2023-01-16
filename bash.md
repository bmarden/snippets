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

## String and Array manipulation

### Add prefix to each element in array

```bash
function addPrefix() {
  prefix="prefix_"
  arr=('first' 'second' 'third')
  echo "${arr[@]/#/$prefix}";
}
```

### Add prefix to each item in args

```bash
function addPrefix() {
  prefix="$2"
  shift 2;
  echo "${@/#/$prefix}"
}

$1 "$@"
```

### Join by string

```bash
joinByString() {
  local separator="$1"
  shift
  local first="$1"
  shift
  printf "%s" "$first" "${@/#/$separator}"
}
```
