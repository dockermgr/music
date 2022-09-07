## 👋 Welcome to music 🚀  

   
  
  
### Requires scripts to be installed

```shell
 sudo bash -c "$(curl -q -LSsf "https://github.com/dockermgr/installer/raw/main/install.sh")"
 dockermgr --config && dockermgr install scripts  
```

OR

### Automatic install/update  

```shell
dockermgr update music
```

#### Just run it

```shell
mkdir -p "$HOME/.local/share/srv/docker/music/"

git clone "https://github.com/dockermgr/music" "$HOME/.local/share/CasjaysDev/dockermgr/music"

cp -Rfva "$HOME/.local/share/srv/docker/music/dataDir/." "$HOME/.local/share/srv/docker/music/"

sudo docker run -d \
--name="music" \
--hostname "music" \
--restart=always \
--privileged \
-e TZ="${TZ:-${TIMEZONE:-America/New_York}}" \
-v "$HOME/.local/share/srv/docker/music/files/data":/data:z \
-v "$HOME/.local/share/srv/docker/music/files/config":/config:z \
-p PORT:INT_PORT \
TEMPLATE/TEMPLATE 1>/dev/null
```

## Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
⛵ dockermgr: [Github](https://github.com/dockermgr) ⛵  
