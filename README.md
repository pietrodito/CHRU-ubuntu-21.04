# CHRU-ubuntu-21.04

## Setup global proxy

``` 
10.50.2.2:3128
```

## Setup APT proxy

```
sudo vi /etc/apt/apt.conf.d/proxy.conf
```

```
Acquire {
  HTTP::proxy  "http://10.50.2.2:3128";
  HTTPS::proxy "http://10.50.2.2:3128";
}
```

## Update ubuntu

```
sudo apt update && sudo apt upgrade -y
```

## Cloning this repo
### ssh local setup

```
ssh-keygen
```

### Copy key to github account

```
cat ~/.ssh/id_rsa.pub
```

Then go   [https://github.com/settings/keys][here]

### Do the cloning

```
sudo apt install -y git
git clone git@github.com:pietrodito/CHRU-ubuntu-21.04.git ~/OS-setup
```

Setup github proxy
