<h1 align="center">👋 Hello there! I'm Robert Rathbun</h1>

<h3 align="center">Cyber Security Architect • Automation Engineer • Zero Trust Practitioner</h3>

<p align="center">
  <a href="https://github.com/rathbunr/rathbunr">
    <img src="https://komarev.com/ghpvc/?username=rathbunr&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views counter" />
  </a>
  <a href="https://github.com/rathbunr?tab=followers">
    <img alt="GitHub followers" src="https://img.shields.io/github/followers/rathbunr?color=green&logo=github&style=flat" />
  </a>
  <a href="https://www.linkedin.com/in/robert-rathbun" target="_blank">
    <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" />
  </a>
</p>

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=0e75b6&center=true&vCenter=true&width=435&lines=Cyber+Security+Architect;Automation+Engineer;Zero+Trust+Practitioner;STIG+Hardening+Expert;Homelab+Enthusiast" alt="Typing SVG" />
</div>

**Cyber Security Architect with 30+ years in enterprise IT, specializing in automation, Zero Trust, and end-to-end secure system builds. I automate everything from hardware provisioning to OS and application deployment, including full STIG hardening using configuration as code. When I’m not working, I’m usually experimenting in my homelab or scuba diving.**

### 🛠️ Example YAML Config (Configuration as Code)
Here's a snippet of how I automate STIG hardening—feel free to adapt for your setups!

```yaml
# Example: Basic Ansible playbook for Zero Trust setup
---
- name: Harden Server with STIG Compliance
  hosts: all_servers
  become: yes
  tasks:
    - name: Update all packages
      apt:
        update_cache: yes
        upgrade: dist
    - name: Enable firewall (UFW)
      ufw:
        state: enabled
        policy: deny
    - name: Install fail2ban for intrusion prevention
      apt:
        name: fail2ban
        state: present
  handlers:
    - name: Restart SSH
      service:
        name: ssh
        state: restarted



