# Install some softwares on the k8s

## Brief

Install and config *.yml* file on the k8s.

Config **ingress** on the k8s so you can access to web local.

If you want to access to domain name, you must edit in `/etc/hosts`. Ex:

`127.0.0.1   localhost`

`127.0.0.1   k8s.prometheus.local`

`127.0.0.1   k8s.loki.local`

## Requirements

If you run on the Linux:

1. Requirements:

   - Platform: *Linux*
   - OS: *Ubuntu*
   - Version: *18.04.03*

2. With **microk8s**:

   - `sudo apt update && sudo apt upgrade -y`
   - `sudo snap install microk8s --classic`

3. With **minikube**:
   - Install [here](https://www.howtoforge.com/tutorial/how-to-install-kubernetes-with-minikube-on-ubuntu-1804-lts/)

If you run on the Windows:

1. [kubernetes.io](https://kubernetes.io/docs/tasks/tools/install-minikube/)
2. [github](https://medium.com/faun/minikube-installation-on-windows-10-9908d17cfad9)

## Installed softwares

1) Grafana
2) Loki
3) Prometheus
4) Redis        **(comming soon)**
5) MySQL        **(comming soon)**
6) Postgres     **(comming soon)**
7) Promtail     **(comming soon)**

## Author

Nickname: Free

Email: noname.spyware@gmail.com

## License

MIT
