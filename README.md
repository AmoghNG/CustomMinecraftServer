# Initial Setup

1. Create user minecraft
```bash
useradd -aG sudo minecraft
```

2. Download this repo at `/home/minecraft/`
```bash
su minecraft
cd ~
git clone https://github.com/AmoghNG/CustomMinecraftServer .
```

# Downloads

1. Download the minecraft 1.16.5
```bash
wget -c https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar
```

2. Download and unzip ngrok; add ngrok API keys found at https://dashboard.ngrok.com/get-started/setup
```bash
wget -c https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
unzip ngrok-stable-linux-amd64.zip
./ngrok authtoken 'authtoken'
```

# Steps to install 

1. Copy `minecraft.service` to `/etc/systemd/system/`
```bash
sudo cp minecraft.server /etc/systemd/system/
```

2. Start the service
```bash
sudo systemctl daemon-reload
sudo systemctl start minecraft.service
sudo systemctl status minecraft.service
```

3. Make server start on boot
```bash
sudo systemctl enable minecraft.service
```
