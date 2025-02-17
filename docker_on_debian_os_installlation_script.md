
## a] Download .deb file
[docker official site](https://docs.docker.com/desktop/setup/install/linux/debian/)

---
---
## b] Set up Docker's apt repository

### Add Docker's official GPG key:
```
sudo apt update
```

```
sudo apt-get install ca-certificates curl
```

```
sudo install -m 0755 -d /etc/apt/keyrings
```

```
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
```

```
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

### Add the repository to Apt sources:
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```
ls /etc/apt/sources.list.d/
```

```
sudo nano /etc/apt/sources.list.d/docker.list
```

---
---
## c] Install the package with apt as follows:
```
sudo apt update
```

```
sudo apt-get install ./docker-desktop-amd64.deb 
```

---
---

## d] Verify installation:
```
docker --version
```

```
sudo docker run hello-world
```
