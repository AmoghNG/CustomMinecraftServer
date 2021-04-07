# Downloads

1. Download the minecraft 1.16.5
```bash
wget -c https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar
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
