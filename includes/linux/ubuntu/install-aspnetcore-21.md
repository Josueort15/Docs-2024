﻿### Ubuntu 20.04 (LTS)

```bash
curl -O https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb
dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

```bash
apt-get update
apt-get install apt-transport-https
apt-get update
apt-get install aspnetcore-runtime-2.1
```

### Ubuntu 19.04

```sh
curl -O https://packages.microsoft.com/config/ubuntu/19.04/packages-microsoft-prod.deb
dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

```sh
apt-get update
apt-get install apt-transport-https
apt-get update
apt-get install aspnetcore-runtime-2.1
```

### Ubuntu 18.04 (LTS)

```sh
curl -O https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb
dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

```sh
add-apt-repository universe
apt-get update
apt-get install apt-transport-https
apt-get update
apt-get install aspnetcore-runtime-2.1
```

### Ubuntu 16.04 (LTS)

```sh
curl -O https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb
dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

```sh
apt-get update
apt-get install apt-transport-https
apt-get update
apt-get install aspnetcore-runtime-2.1
```
