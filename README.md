# Automating Minikube with Jenkins

#### Prerequisite
- User Account with Sudo Privileges
- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection
- Container or virtual machine manager, such as: Docker, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox, or VMWare

### 1.) Minikube
#### 1.1.) Install Minikube
- Run as user ubuntu

Exec command:
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
```

#### 1.2.) Start Minikube
- Run as user ubuntu

Exec command:
```
minikube start
```

### 2.) Jenkins
#### 2.1.) Install Java
- Run as user ubuntu

Exec command:
```
sudo apt update
sudo apt install openjdk-8-jdk -y
```

#### 2.2.) Add Jenkins Repository
- Run as user ubuntu

Exec command:
```
wget –q –O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add –
sudo vi /etc/apt/sources.list
#  Jenkins software repository
deb https://pkg.jenkins.io/debian binary  --> add this line
```

#### 2.3.) Install Jenkins
- Run as user ubuntu

Exec command:
```
sudo apt update
sudo apt install jenkins
sudo systemctl status jenkins
```
Open jenkins on your browser:
```
http://127.0.0.1:8080
## Unlock your jenkins by copy the default password
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
