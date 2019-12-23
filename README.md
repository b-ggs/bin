# bin

🗑️ bash and python3 binaries for things and stuff

## Usage

Just run the binaries.

Alternatively, run `bin/symlink` _(requires python3)_ to symlink all the binaries to `/usr/local/bin`.

## Binaries

### autorsync (sh)

Similar to `autossh`, this just repeatedly runs rsync when it exits with a non-zero code

#### Usage

```bash
autorsync [RSYNC_OPTIONS]
```

### flatten_dir (python3)

Moves all nested files in a specified directory into itself

#### Usage

```bash
$ find /tmp/1
/tmp/1
/tmp/1/1
/tmp/1/1/1
/tmp/1/1/1/1
/tmp/1/1/1/1/file.txt

$ flatten_dir -n /tmp/1
Will move /tmp/1/1/1/1/file.txt -> /tmp/1/file.txt
Will delete /tmp/1/1/1/1
Will delete /tmp/1/1/1
Will delete /tmp/1/1

$ flatten_dir -f /tmp/1
Moving /tmp/1/1/1/1/file.txt -> /tmp/1/file.txt
Deleting /tmp/1/1/1/1
Deleting /tmp/1/1/1
Deleting /tmp/1/1

$ find /tmp/1
/tmp/1
/tmp/1/file.txt
```
