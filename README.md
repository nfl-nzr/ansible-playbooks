# Ansible playbooks to setup home server
Runs media server on master node. Currently does the following
- Installs dependencies
- Sets up docker gpg keys & and adds docker repo
- Installs docker & compose
- Clones media_server repo and creates env variables
- Updates fstab and mounts hdd with config and data
- Starts docker demon
- Runs arr apps

Secrets: 
place vault.yml in group_vars/all/vault.yml
```
git_username: git user
git_token: gittoken
cloudflare_tunnel_token: cloudflared tunnel token
```
Wireguard config:
Place wireguard conf file in /roles/start_services/files/
This will setup a wireguard proxy for jackett

