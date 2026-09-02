### Install Docker ###

#### Set up Docker's **apt** repositotr ####  

`sudo apt update`  
`sudo apt install ca-certificates curl`  
`sudo install -m 0755 -d /etc/apt/keyrings`  
`sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc`  
`sudo chmod a+r /etc/apt/keyrings/docker.asc`  

#### Add the repository to apt sources ####
	sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
		Types: deb
		URIs: https://download.docker.com/linux/debian
		Suites: trixie
		Components: stable
		Architectures: $(dpkg --print-architecture)
		Signed-By: /etc/apt/keyrings/docker.asc
	EOF

`sudo apt update`  
`sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`  
`sudo systemctl status docker`  
`sudo systemctl start docker`  
`sudo docker run hello-world`  










# Header 1 # 
**Bold**

## Header 2 ## 
*Italics*

### Header 3 ### 
***Bold Italics***

testing  
	`code` snippet  
conmtiunef  



List
- 1
	- 1.1
	- 1.2
- 2
- 3

sudo apt remove $(dpkg --get-selections docker.io docker-compose docker-doc docker-buildx podman-docker containerd runc | cut -f1)

`apt install sudo -y`
`apt update`
`usermod -aG sudo $USER`
`nano /etc/network/interfaces`

	auto ens18
    iface ens18 inet static
        address 10.0.0.X
	netmask 255.255.255.0
        gateway 10.0.0.1
        dns-nameservers 1.1.1.1 8.8.8.8


`systemctl restart networking`

# ssh into command prompt #
ssh {user}@{IP}

# Helpful Tools to install #
`sudo apt install -y curl net-tools wget git htop unzip zip ca-certificates gnupg tree`
`sudo apt update`


# General Docker Install #
`mkdir docker`
`cd docker`


`sudo install -m 0755 -d /etc/apt/keyrings`
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/debian bookworm stable" \
  | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo docker run hello-world

sudo usermod -aG docker $USER
newgrp docker



sudo nano docker-compose.yml
sudo nano env # based on need

docker compose up -d

# for arr stack # 
sudo mkdir -p /data/{media/{tv,movies,music,books},downloads/{complete/{tv,movies,music,books},incomplete/{tv,movies,music,books}}}
sudo mkdir -p /data/media/{tv,movies,music,books}



tree /data
sudo chown -R 1000:1000 /data
sudo chmod -R a=,a+rX,u+w,g+w /data
ls -ln /data


sudo docker logs qbittorrent


