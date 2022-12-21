# Docker To Podman

Old habits... having "cut my teeth" on OpenShift 3, I was initiated by using "docker".  Now that I use podman, I have created a work-around until I break myself of the habit of typing "docker <do something".  Next up:  replacing 'oc' with 'kubectl'.  

This is what I have done to mitigate my faux pas.

```
( which podman ) || { sudo yum -y install podman; }
sudo systemctl enable podman --now
alias | grep podman || { echo "alias docker=$(which podman)" >> ~/.bashrc.d/fedora; . ~/.bashrc; }
docker info
docker pull centos:latest
docker images
```

