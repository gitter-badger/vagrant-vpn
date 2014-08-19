vagrant-vpn
===========

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

