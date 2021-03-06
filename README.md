# Watchman

1. Serves static content.
2. Reloads and reservers content automatically when file content changes.

Works only on Linux and Unix systems.

### Serve static html content

```bash
watchman server
```

Starts a web server at port 8000 to serve static html content.

### Watch for file content changes

```bash
watchman watch
```

Starts a web server at port 8000 to serve static html content and reloads when
changes happen to the file content.


Helps in auto reloading of changes. Changes can be previewed without restarting
the server. Make changes to the html files and hit browser refresh to see the changes.
Save time while development html based apps.

### Options

`-d` for target Directory (by default current directory is considered for serving or watching)

`-p` for port on which the sever has to be run

```bash
[watchman] watchman -d ~/ -p 2000 server                            master  ✭
Serving from directory "/Users/foobar/"
Listening on http://127.0.0.1:2000
```

### Build

#### Install stack

```bash
curl -sSL https://get.haskellstack.org/ | sh
```

    or

```bash
wget -qO- https://get.haskellstack.org/ | sh
```

#### Download the code or use git to clone code repo

```bash
git clone https://github.com/pamu/watchman.git
```

    or

```bash
git clone git@github.com:pamu/watchman.git
```

#### Go to project folder

```bash
cd watchman
```

#### Stack build


```bash
stack build
```

#### Stack install

in the same project root folder (inside watchman directory)

```bash
stack install
```

The above command will create a executable called `watchman` and put the executable in
`.local/bin` folder in your home directory.

#### Export PATH

```bash
export PATH="~/.local/bin/:$PATH"
```

Now you can access `watchman` from you command line.
