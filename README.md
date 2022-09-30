## 👋 Welcome to navidrome 🚀  

   
  
  
### Requires scripts to be installed

```shell
 sudo bash -c "$(curl -q -LSsf "https://github.com/dockermgr/installer/raw/main/install.sh")"
 dockermgr --config && dockermgr install scripts  
```

OR

### Automatic install/update  

```shell
dockermgr update navidrome
```

#### Just run it

```shell
mkdir -p "$HOME/.local/share/srv/docker/navidrome/"

git clone "https://github.com/dockermgr/navidrome" "$HOME/.local/share/CasjaysDev/dockermgr/navidrome"

cp -Rfva "$HOME/.local/share/srv/docker/navidrome/dataDir/." "$HOME/.local/share/srv/docker/navidrome/"

sudo docker run -d \
--name="navidrome" \
--hostname "navidrome" \
--restart=always \
--privileged \
-e TZ="${TZ:-${TIMEZONE:-America/New_York}}" \
-v "$HOME/.local/share/srv/docker/navidrome/files/data":/data:z \
-v "$HOME/.local/share/srv/docker/navidrome/files/config":/config:z \
-p PORT:INT_PORT \
TEMPLATE/TEMPLATE 1>/dev/null
```

## Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
⛵ dockermgr: [Github](https://github.com/dockermgr) ⛵  
