# 🚀 CI/CD Deployment to EC2 via GitHub Actions

This project demonstrates automatic deployment of a static web page to an EC2 instance using GitHub Actions.

---

## 🛠 Setup

1. **Launch EC2 (Amazon Linux 2)**  
   - Install NGINX:  
     ```bash
     sudo amazon-linux-extras install nginx1 -y
     sudo systemctl start nginx
     sudo systemctl enable nginx
     sudo chmod -R 755 /usr/share/nginx/html
     ```

2. **Configure GitHub Secrets**
   - `EC2_HOST`: Public IP
   - `EC2_USER`: Usually `ec2-user`
   - `EC2_KEY`: Private `.pem` file content

3. **GitHub Actions Workflow**
   - Located at `.github/workflows/deploy.yml`
   - Deploys `index.html` to EC2 on every push to `main`

---

## 🚀 Deploy

1. Update `index.html`
2. Commit & push to `main`
3. Visit: `http://<EC2_PUBLIC_IP>`

---

👨‍💻 Built by Ajith from Xops
