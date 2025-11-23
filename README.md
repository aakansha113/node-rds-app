# Node-RDS-App

### Project Structure

node-rds-app/
│── node_modules/
│── public/
│       |── index.html
|       |── script.js
|       |── style.css
│── src/
│       |── routes.js
|       |── app.js
|       |── database.js
│── .dockerignore
│── Dockerfile
│── README.md
│── package-lock.json
│── package.json

### 📥 Clone This Repository
#### To clone this portfolio on your local system, run:
```
git clone https://github.com/aakansha113/my-portfolio.git
```
### step1:Install Dependencies (Optional for Local Run):
```
npm install
node src/server.js
```

### Step2:Build and Run Docker Image:
```
docker build -t node-rds-app .
```
### Step3:AWS RDS Setup:
-Create an RDS instance (MySQL)
-Note endpoint, username, password
-Update EC2 security group to allow inbound MySQL (3306)

### Step4:Deploy on AWS EC2:

### Step 1: Launch EC2 Instance:
Amazon Linux 2 or Ubuntu
Open ports: 3000 (HTTP), 3306 (MySQL) in Security Group

### Step 2: Install Docker on EC2:
```
sudo yum update -y
sudo yum install docker -y
sudo service docker start
sudo usermod -aG docker ec2-user
```

### Step 3: Deploy Application:
```
docker pull <your-docker-image>   
```
### Step 4: Run the imgage:

```
docker run --rm -p 80:3000 \
-e DB_HOST="your-db-hostname" \
-e DB_USER="your-db-username" \
-e DB_PASSWORD="your-db-password" \
-d aakansha113/node-rps-app:v1 
```
### ⭐ Show Your Support
#### If you like this portfolio, feel free to ⭐ star the repo!
