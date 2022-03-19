# ssh
## generate new ssh key pair
`ssh-keygen -t ed25519 -C "your_email@example.com"`

 generate new ssh key pair on legacy system
`ssh-keygen -t ras -b 4096 -C "your_email@example.com"` 

## add ssh key to ssh-agent
1. start ssh-agent in the background
`eval "$(ssh-agent -s)"`
this will print the agent process id
2. add ssh private key to ssh-agent
`ssh-add ~/.ssh/id_ed25519`

## use X11 to run gui applications remotely
1. allow X11 forwarding in your ssh config by uncommenting the line `X11Forwarding yes` in `/etc/ssh/sshd_config` on the remote server

2. restart ssh server
```bash
sudo systemctl restart sshd
```

3. specify X forwarding on client end when establishing ssh connection
```bash
ssh -X username@server
```

## links
- [make use of article](https://www.makeuseof.com/run-graphical-x-apps-over-ssh-linux/#:~:text=SSH%20makes%20it%20easy%20and,display%20them%20on%20your%20machine.)

*Note: this tends to be slow*
