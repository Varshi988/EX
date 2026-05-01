# DEVOPS LAB EXAM PREPARATION (Study Friendly – First Time Learner)

I converted your **DevOps Manual** into easy exam format: **Question/Aim + Step-by-Step Process** only, with clean short points so you can perform any experiment in morning exam. 

---

# EXPERIMENT 1

## Aim: Implement Continuous Integration with Version Control

### Steps:

1. Create project folder.
2. Open terminal inside folder.
3. Initialize Git:

```bash
git init
```

4. Create Python file:

```python
# app.py
def add(a,b):
    return a+b
```

5. Add files:

```bash
git add .
```

6. Commit:

```bash
git commit -m "Initial Commit"
```

7. Create GitHub repo.
8. Connect remote:

```bash
git remote add origin <repo_url>
```

9. Push:

```bash
git branch -M main
git push -u origin main
```

10. Create folder:

```bash
.github/workflows/
```

11. Create file:

```bash
ci.yml
```

12. Add CI workflow YAML.
13. Push again.
14. Open GitHub → Actions tab → Check build status.

---

# EXPERIMENT 2

## Aim: Setup Scrum / Kanban Board

### Steps:

1. Open Trello / Jira / GitHub Projects.
2. Create new board.
3. Select Scrum or Kanban.
4. Create columns:

**Scrum:**
Backlog → To Do → In Progress → Done

**Kanban:**
To Do → In Progress → Review → Completed

5. Add tasks as cards.
6. Move cards based on work progress.
7. Review tasks daily.

---

# EXPERIMENT 3

## Aim: Implement Continuous Testing using Jenkins

### Steps:

1. Install Java, Maven, Git, Jenkins.
2. Open Jenkins:

```bash
http://localhost:8080
```

3. Create sample Maven project.
4. Write Java code and test case.
5. Initialize Git:

```bash
git init
git add .
git commit -m "Initial"
```

6. Open Jenkins.
7. Create Freestyle Project.
8. Add Git repository URL.
9. Build step:

```bash
mvn clean test
```

10. Save project.
11. Run Build Now.
12. Check console output and test result.

---

# EXPERIMENT 4

## Aim: Explore Git and GitHub Commands

### Steps:

1. Check Git:

```bash
git --version
```

2. Configure:

```bash
git config --global user.name "Name"
git config --global user.email "mail@gmail.com"
```

3. Create repo:

```bash
mkdir myproject
cd myproject
git init
```

4. Create file:

```bash
echo Hello > file.txt
```

5. Add & commit:

```bash
git add .
git commit -m "First Commit"
```

6. Push to GitHub.
7. Clone:

```bash
git clone <url>
```

---

# EXPERIMENT 5

## Aim: Create New Git Repository and Push README

### Steps:

1. Create folder and open terminal.
2. Initialize:

```bash
git init
```

3. Create README:

```bash
echo "# My Repo" > README.md
```

4. Add:

```bash
git add README.md
```

5. Commit:

```bash
git commit -m "Added README"
```

6. Create repo in GitHub.
7. Connect remote:

```bash
git remote add origin <url>
```

8. Push:

```bash
git branch -M main
git push -u origin main
```

---

# EXPERIMENT 6

## Aim: Create Branch "MITS" and Merge

### Steps:

1. Initialize repo:

```bash
git init
```

2. Create branch:

```bash
git checkout -b MITS
```

3. Create file:

```bash
echo Hello > sample.txt
```

4. Add & commit:

```bash
git add .
git commit -m "Added sample file"
```

5. Return main:

```bash
git checkout main
```

6. Merge:

```bash
git merge MITS
```

7. Delete branch:

```bash
git branch -d MITS
```

---

# EXPERIMENT 7

## Aim: Use Git Log and Find Commit Hash

### Steps:

1. Open repository folder.
2. Show history:

```bash
git log
```

3. Short format:

```bash
git log --oneline
```

4. Copy commit hash.
5. Show details:

```bash
git show <hash>
```

---

# EXPERIMENT 8

## Aim: Clone Git Repository

### Steps:

1. Copy repository URL.
2. Open terminal.
3. Run:

```bash
git clone <repo_url>
```

4. Enter folder:

```bash
cd repo-name
```

5. Check remote:

```bash
git remote -v
```

---

# EXPERIMENT 9

## Aim: Push Local Changes to Remote Repository

### Steps:

1. Create repo:

```bash
git init
```

2. Create file:

```bash
echo Hello > file.txt
```

3. Add:

```bash
git add .
```

4. Commit:

```bash
git commit -m "Initial Commit"
```

5. Connect GitHub:

```bash
git remote add origin <url>
```

6. Push:

```bash
git branch -M main
git push -u origin main
```

---

# EXPERIMENT 10

## Aim: Inspect Google Element using Selenium

### Steps:

1. Install Selenium:

```bash
pip install selenium
```

2. Install Edge driver.
3. Python code:

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Edge()
driver.get("https://google.com")

box = driver.find_element(By.NAME,"q")
print(box)

driver.quit()
```

---

# EXPERIMENT 11

## Aim: Facebook Login using Selenium

### Steps:

1. Install Selenium.
2. Code:

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time

driver = webdriver.Edge()
driver.maximize_window()

driver.get("https://www.facebook.com/")

wait = WebDriverWait(driver, 20)

email = wait.until(EC.visibility_of_element_located((By.NAME, "email")))
password = wait.until(EC.visibility_of_element_located((By.NAME, "pass")))

email.send_keys("your_email")
password.send_keys("your_password")

login = wait.until(EC.element_to_be_clickable((By.NAME, "login")))
login.click()

time.sleep(10)

print("Facebook homepage opened successfully")

driver.quit()
```

---

# EXPERIMENT 12

## Aim: Test Google Homepage Elements

### Steps:

1. Open Google using Selenium.
2. Locate Search box.
3. Type text.
4. Press Enter.
5. Find buttons and links.
6. Close browser.

---

# EXPERIMENT 13

## Aim: Basic Docker Commands

### Steps:

```bash
docker --version
docker pull ubuntu
docker images
docker run -it ubuntu
docker ps
docker ps -a
docker stop <id>
docker start <id>
docker rm <id>
docker rmi ubuntu
```

---

# EXPERIMENT 14

## Aim: Run HTML Webpage using Docker

### Steps:

1. Create `index.html`

```html
<h1>Hello World</h1>
```

2. Create Dockerfile:

```dockerfile
FROM nginx
COPY index.html /usr/share/nginx/html/
```

3. Build:

```bash
docker build -t myapp .
```

4. Run:

```bash
docker run -d -p 8080:80 myapp
```

5. Open browser:

```bash
localhost:8080
```

---

# EXPERIMENT 15

## Aim: Alpine Image with Nano

### Steps:

1. Create Dockerfile:

```dockerfile
FROM alpine
RUN apk add --no-cache nano
CMD ["/bin/sh"]
```

2. Build:

```bash
docker build -t alpine-nano .
```

3. Run:

```bash
docker run -it alpine-nano
```

4. Check:

```bash
nano --version
```

---

# EXPERIMENT 16

## Aim: Run MySQL in Docker

### Steps:

1. Pull image:

```bash
docker pull mysql
```

2. Run:

```bash
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -d mysql
```

3. Enter MySQL:

```bash
docker exec -it mysql-container mysql -uroot -proot
```

4. Commands:

```sql
CREATE DATABASE student_db;
USE student_db;
CREATE TABLE students(id int,name varchar(20));
INSERT INTO students VALUES(1,'Ram');
SELECT * FROM students;
```

---

# EXPERIMENT 17

## Aim: MySQL with phpMyAdmin

### Steps:

1. Create network:

```bash
docker network create mynetwork
```

2. Run MySQL:

```bash
docker run --name mysql-container --network mynetwork -e MYSQL_ROOT_PASSWORD=root -d mysql
```

3. Run phpMyAdmin:

```bash
docker run --name phpmyadmin --network mynetwork -p 8080:80 -d phpmyadmin/phpmyadmin
```

4. Open browser:

```bash
localhost:8080
```

5. Login:

* Username: root
* Password: root

---

# MOST IMPORTANT VIVA QUESTIONS

### Git

* What is Git?
* Difference between Git and GitHub?
* What is commit? branch? merge?

### Jenkins

* What is CI/CD?
* Why Jenkins used?

### Selenium

* What is WebDriver?
* What are locators?

### Docker

* Difference image vs container?
* What is Dockerfile?

### MySQL

* What is database? table? primary key?

---

# FINAL EXAM STRATEGY (8 HOURS)

### First 3 Hours:

Read Exp 4 to 9 (Git full)

### Next 2 Hours:

Read Exp 13 to 17 (Docker full)

### Next 2 Hours:

Read Selenium (10-12)

### Last 1 Hour:

Read Jenkins + Viva

---

If you want, I can also make **"Most Repeated DevOps Lab External Questions with Exact Answers PDF style notes"** for tomorrow exam.
