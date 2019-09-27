## SSH

SSH is the Secure Shell, a cryptographic network protocol. It uses public-key cryptography to authenticate the remote computer and optional user name. The user must prove his/her identity to the remote machine.
SSH is typically used to log into and execute commands in a remote machine .

Basic syntax, will prompt for password:
```bash
$ ssh <remote_user>@<remote_host>
```

Commonly if you are using AWS you will SSH while also passing your private key, using the `-i`option

```bash
$ ssh -i ~/.ssh/key.pem -tt ubuntu@ec2-54-93-188-105.eu-central-1.compute.amazonaws.com
```

## SSH tunneling for jupyter notebooks

```bash
$ ssh -N -L localhost:8888:localhost:8888 <remote_user>@<remote_host>
```

More details: 
* [Running a Jupyter notebook from a remote server](https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/)
* [5 Ways to Keep Remote SSH Sessions and Processes Running After Disconnection](https://www.tecmint.com/keep-remote-ssh-sessions-running-after-disconnection/)