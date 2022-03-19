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
