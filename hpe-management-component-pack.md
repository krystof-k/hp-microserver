# HPE Management Component Pack

```console
sudo apt update
sudo apt upgrade

sudo bash -c 'cat <<EOF > /etc/apt/sources.list.d/hpe.list
# HPE Management Component Pack
deb http://downloads.linux.hpe.com/SDR/repo/mcp bionic/10.80 non-free
EOF'

curl https://downloads.linux.hpe.com/SDR/hpPublicKey2048.pub | sudo apt-key add -
curl https://downloads.linux.hpe.com/SDR/hpPublicKey2048_key1.pub | sudo apt-key add -
curl https://downloads.linux.hpe.com/SDR/hpePublicKey2048_key1.pub | sudo apt-key add -

sudo apt update
sudo apt install hp-ams
```
