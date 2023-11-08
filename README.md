# LAVA Validator setup
## 1.Hardware required
![image](https://github.com/Adamtruong6868/LAVA/assets/91002010/26a6b8b2-10be-4991-b84d-a2edb4e4619c)

## 2.Set Validator nam
```php
MONIKER="Your-name_VNBnode"
```
## 3.Update system
```php
sudo apt -q update
sudo apt -qy install curl git jq lz4 build-essential
sudo apt -qy upgrade
```
## 4. Install Go version 1.20.5
```php
sudo rm -rf /usr/local/go
curl -Ls https://go.dev/dl/go1.20.5.linux-amd64.tar.gz | sudo tar -xzf - -C /usr/local
eval $(echo 'export PATH=$PATH:/usr/local/go/bin' | sudo tee /etc/profile.d/golang.sh)
eval $(echo 'export PATH=$PATH:$HOME/go/bin' | tee -a $HOME/.profile)
echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> $HOME/.bash_profile
source $HOME/.bash_profile
go version
```
## 5. Install GCC
```php
sudo apt install build-essential
```
## 6. Install all Binaries 🛠️
```php
git clone https://github.com/lavanet/lava.git
cd lava
make install-all
```
### Check version
```php
lavad version && lavap version
```
## 7.Build all Binaries
```php
make build-all
```
