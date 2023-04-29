# Docker CentOS + SSHD
https://hub.docker.com/r/jdeathe/centos-ssh

docker run -d -p 2021:22 --name ssh1 jdeathe/centos-ssh
docker run -d -p 2022:22 --name ssh2 jdeathe/centos-ssh

ssh -p 2021 -i id_rsa_insecure app-admin@localhost
ssh -p 2022 -i id_rsa_insecure app-admin@localhost

ssh -p 22 -i id_rsa_insecure app-admin@

# Docker Apline + SSHD
https://hub.docker.com/r/sickp/alpine-sshd/

docker run --rm -d -p 2222:22 sickp/alpine-sshd

// root / root
// If case of ssh keys issue -> drop in known_hosts
// cat /dev/null > ~/.ssh/known_hosts
ssh root@localhost -p 2222
ssh root@172.17.0.2 -p 22

# Dockerized Python+SSH image
https://github.com/David-Lor/Dockerized-Python-SSH

docker run -d -p 2221:22 --name pythonssh1 davidlor/python-ssh
ssh pythonssh@172.17.0.2 -p 22 // pass: sshpass


