Installation of Trivy "A Simple and Comprehensive Vulnerability Scanner for Containers and other Artifacts, Suitable for CI" on Ubuntu.

# Trivy Installation
```
sudo apt-get -y install wget apt-transport-https gnupg lsb-release
```{{exec}}

```
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null
echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy
```{{exec}}
