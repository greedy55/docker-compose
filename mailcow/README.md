# Mailcow Install
*****
*Clone the master branch of the repository, make sure your umask equals 0022. Please clone the repository as root user and also control the stack as root. We will modify attributes - if necessary - while bootstrapping the containers automatically and make sure everything is secured. The update.sh script must therefore also be run as root. It might be necessary to change ownership and other attributes of files you will otherwise not have access to. We drop permissions for every exposed application and will not run an exposed service as root! Controlling the Docker daemon as non-root user does not give you additional security. The unprivileged user will spawn the containers as root likewise. The behaviour of the stack is identical.*
*****
*****
[!INFO]  
**RUN AS ROOT**
*****
##### [Mailcow-Help](https://docs.mailcow.email/i_u_m/i_u_m_install/#check-selinux-specifics)
*****
*****
```
cd /opt
git clone https://github.com/mailcow/mailcow-dockerized
cd mailcow-dockerized
```
*****
#### Generate a configuration file. Use a FQDN (host.domain.tld) as hostname  
```
./generate_config.sh
```
##### Change -entrapments-  
```
nano mailcow.conf
```
*****
*****
### Start Mailcow Containers
```
docker compose pull
docker compose up -d
```
*****