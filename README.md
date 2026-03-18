# Automated Website Deployment with Ansible

This project demonstrates how to automate the deployment of a static website (HTML, CSS, JS) using Ansible, configure Nginx to serve the website, and set up SSL using Let's Encrypt.

## **Technologies Used**

- **Ansible**: Automation tool for configuration management and deployment.
- **Nginx**: Web server for hosting the website.
- **Certbot**: Tool to obtain SSL certificates from Let's Encrypt.

## **Project Setup**

### Prerequisites

1. **Ansible** installed on your local machine or control node.
2. A **remote server** (Ubuntu is recommended) with **SSH access**.
3. A **GitHub repository** with your website files (HTML, CSS, JS).
4. **A domain name** configured to point to the server (for SSL, optional).

### Steps to Deploy the Website

1. Clone the website repository to the server.
2. Install necessary software (Nginx, Git, Certbot).
3. Configure Nginx to serve the website.
4. Set up **SSL certificates** using **Let's Encrypt**.
5. **Automatic SSL certificate renewal**.

### Running the Playbook

To deploy the website, use the following command:
ansible-playbook -i inventory/hosts.ini playbooks/site.yml

```bash
ansible-playbook -i inventory/hosts.ini playbooks/site.yml

ansible-website/
├── inventory/
│   └── hosts.ini      # Hosts configuration
├── playbooks/
│   └── site.yml       # Main playbook
├── roles/
│   └── webserver/
│       ├── tasks/
│       │   └── main.yml
│       ├── templates/
│       │   └── nginx.conf.j2
└── README.md
