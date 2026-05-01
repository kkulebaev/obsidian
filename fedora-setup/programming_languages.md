## Go (-)

```sh
sudo dnf install golang
```

## Node.js
На Fedora 40 уже установлен node.js

Node.js is available as a module called `nodejs` in CentOS/RHEL 8 and Fedora.

```bash
sudo dnf module install nodejs:<stream>
```

where `<stream>` corresponds to the major version of Node.js. To see a list of available streams:

```bash
dnf module list nodejs
```

For example, to install Node.js 18:

```bash
sudo dnf module install nodejs:18/common
```