vagrant-vpn
===========
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/dstokes/vagrant-vpn?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Use vagrant to make working over VPN less painful

usage
=====
```sh
vagrant up && vagrant ssh
```
once you're in the machine start a tmux session and openvpn:
```sh
openvpn --config /etc/vpn_profiles/your-profile.ovpn
```
then ssh to a machine withing the vpn:
```
ssh -i /etc/host_ssh/your-key.pem user@host
```

setup
=====
1. copy your vpn config files to `./profiles`
2. start up vagrant

