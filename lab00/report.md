## Tasks and commands

### 1. Navigating the system

```bash
cd ~
mkdir linux-exercise
cd linux-exercise
```

Moved to the home directory, created `linux-exercise` and entered it.

### 2. Working with files and directories

```bash
echo "Anže Šavli" > description.txt
cat description.txt
mkdir test
mv description.txt ./test
cd ./test
ls
```

Created `description.txt` containing my name, created the `test` directory and moved the file into it. `cat` confirmed the contents.

### 3. Moving and copying

```bash
mv description.txt my_profile.txt
cp my_profile.txt ~/
```

Renamed the file to `my_profile.txt` and copied it to the home directory. `ls` and `cat` in `~` confirmed the copy.

### 4. Permissions and sizes

```bash
du -ah .
chmod 444 test/my_profile.txt
ll
```

`du -ah` listed the size of every file and folder (mostly small cache files, e.g. `.cache/gstreamer-1.0` at 1.4M). `chmod 444` made `test/my_profile.txt` read-only for owner, group and others.

### 5. System information

```bash
whoami
du -sh ~
df -h
```

| Item | Result |
|---|---|
| Username | `kali` |
| Home directory size | 34M (`/home/kali`) |
| Root filesystem (`/dev/sda1`) | 79G total, 17G used, **59G available** (22% used) |

### Extra task: largest items in the home directory

```bash
du -ah ~ | sort -rh | head -n 5
```

| Size | Path |
|---|---|
| 34M | `/home/kali` |
| 17M | `/home/kali/.mozilla/firefox/6dkq3m3i.default-esr` |
| 17M | `/home/kali/.mozilla/firefox` |
| 17M | `/home/kali/.mozilla` |
| 15M | `/home/kali/.cache` |
