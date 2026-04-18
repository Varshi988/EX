Experiment No- 1
AIM:
Implementing Continuous Integration with Version Control
Objective:
To implement Continuous Integration (CI) using Git for version control and GitHub Actions for CI workflow
automation.
Software/Hardware Requirements:
- Computer with Linux/Windows OS
- Internet Connection
- Git installed
- GitHub account
- Code editor (VSCode, PyCharm, or any preferred editor)
Theory:
In DevOps, Version Control Systems (VCS) and Continuous Integration (CI) play a crucial role in automating
software delivery pipelines.
1. Version Control System (VCS):
- Tracks source code changes over time.
- Supports collaboration among developers.
- Example: Git (most widely used VCS).
2. Continuous Integration (CI):
- A practice where developers frequently integrate code into a shared repository.
- Automated builds and tests are triggered on every push or pull request.
- Helps detect integration errors early.
3. GitHub Actions:
- A CI/CD platform integrated with GitHub repositories.
- Enables automated workflows like code build, test, and deployment.
- Workflows are defined using YAML files.

Algorithm:
Algorithm / Procedure:
Step 1: Initialize Git Repository (Local Version Control Setup)
- Create a project folder.
- Open terminal and navigate to the folder.
- Run: git init
- Create a simple Python file (example: app.py) with basic code and a test case.
- Stage and commit changes:
git add .
git commit -m "Initial Commit"
Step 2: Push to Remote Repository (GitHub Integration)
- Create a new repository on GitHub (name: ci-lab-demo).
- Link local repository to GitHub:
git remote add origin https://github.com/username/ci-lab-demo.git
- Push the code to GitHub:
git branch -M main
git push -u origin main
Step 3: Configure CI Pipeline (GitHub Actions)
- Create a directory .github/workflows/ in the project.
- Create a file ci-pipeline.yml in that folder.
- Add the following YAML to define CI workflow:
(name: CI Pipeline)
(on: push and pull_request to main branch)
(jobs: build with ubuntu-latest)
(steps include: checkout code, setup python, install dependencies, run tests)
Step 4: Trigger and Observe CI Execution
- Commit and push .github/workflows/ci-pipeline.yml file.
- Visit GitHub > Actions tab to see the pipeline triggered.
- Observe results: Success if all tests pass, Failure if any test fails.
Sample Code (app.py):
def add(a, b):
return a + b
def test_add():
assert add(2, 3) == 5
Result:
The experiment was successfully completed, and Continuous Integration (CI) pipeline was implemented
using GitHub Actions along with Git version control. Each code change triggered an automated build and test
process.
Observation:
| Step | Observation |
|---|---|
| Git Initialization | Local repository initialized successfully |
| Push to GitHub | Code visible on GitHub |
| CI Workflow Added | Workflow file committed and pushed |
| CI Execution | Automated build and test run visible in Actions tab |
| Final Output | Success (Green Tick) on passing tests |
Viva Questions:
- What is the role of version control in DevOps?
- Define Continuous Integration (CI).
- Explain the structure of a GitHub Actions workflow file.
- Why is YAML used in CI configuration?
- How does GitHub Actions detect new code changes?
Conclusion:
This experiment demonstrated how to set up version control using Git and implement a continuous
integration pipeline using GitHub Actions. This ensures every code commit is automatically verified through
tests, improving code quality and enabling faster releases.

Advantages:
- Automated testing ensures fewer bugs reach production.
- Developers get fast feedback on code changes.
- Integration issues are detected early.
Applications:
- Modern software development teams use CI in every project.
- Essential in Agile and DevOps workflows.
- Used in Open Source projects to maintain code quality.


Experiment No- 2
AIM:
Setting Up a Scrum or Kanban Board for Task Management
Objective:
To learn and demonstrate the process of setting up and using a Scrum Board or Kanban Board for effective task management in software development projects. These boards help teams visualize work, improve collaboration, and maintain continuous delivery, which is especially useful in Agile environments.
Software/Hardware Requirements:
- Computer with Linux/Windows OS
- Internet Connection
- Trello / Jira / GitHub Projects account
- Web Browser
Theory:
In Agile Project Management, teams use visual boards to manage tasks and workflows effectively. Two
popular methodologies are Scrum and Kanban.
1. Scrum Board:
- Scrum is a framework used for iterative development.
- Work is divided into Sprints (short development cycles, typically 1-4 weeks).
- A Scrum Board visually tracks tasks through stages like: Backlog, To Do, In Progress, Done.
- Scrum Boards are typically reset at the start of each sprint, ensuring they only show work planned for the
current sprint.
2. Kanban Board:
- Kanban focuses on continuous delivery.
- Work items flow continuously through stages without fixed sprints.
- A Kanban Board tracks tasks through customizable stages like: To Do, In Progress, Review, Completed.
- Kanban Boards are continuous, meaning tasks are added and completed without resetting the board.
Algorithm:
Algorithm / Procedure:
1. Choose a Tool
- Open Trello, Jira, or GitHub Projects.
- Create a new board for your project.
2. Define Board Type
- Select either Scrum Board or Kanban Board based on your process needs.
3. Create Columns (Workflow Stages)
- The columns should reflect the actual workflow followed by your team.
- Scrum: Product Backlog, Sprint Backlog, To Do, In Progress, Done
- Kanban: To Do, In Progress, Review, Completed
4. Add Tasks (Cards)
- Add individual tasks as cards in appropriate columns.
- Each task should have: Title, Description, Assignee, Due Date (optional)
5. Track and Update Tasks
- Move cards across columns to track progress.
- Use daily standups (Scrum) or regular syncs (Kanban).
6. Review and Retrospect
- Review the board after each sprint (Scrum) or periodically (Kanban).
- Discuss improvements and bottlenecks.
Sample Board Screenshot (Example Layout):
| Column | Example Task |
|----------------|-------------------------------|
| Product Backlog | Define Login API |
| Sprint Backlog | Set up Database Schema |
| To Do | Create Frontend UI |
| In Progress | Implement User Authentication |
| Done | Set Up Project Repository |
Result:
The experiment was successfully completed, and a Scrum/Kanban Board was created using
Trello/Jira/GitHub Projects. The team learned how to visually manage tasks and improve workflow
transparency.
Observation Table:
| Step | Observation |
|----------------|----------------|
| Board Creation | New board created successfully |
| Columns Added | Workflow stages added correctly |
| Tasks Created | Cards added with details (title, description, assignee) |
| Task Movement | Cards moved across columns to reflect progress |
Conclusion:
This experiment demonstrated how to set up and use a Scrum or Kanban Board for effective task
management. By visualizing work items and tracking their progress, teams can collaborate better, identify
bottlenecks early, and improve productivity. Both boards also help teams adapt to changing requirements,
which is a key benefit in Agile development.

Experiment No- 3
AIM:
Implementing Continuous Testing in the DevOps Lifecycle
Objective:
To implement Continuous Testing in the DevOps lifecycle using Jenkins and Maven for a sample project.
The process will automatically test the project whenever new code is pushed to the repository, ensuring continuous quality Software/Hardware Requirements:
- Operating System: Windows / Linux
  Tools:
- Java
- Maven
- Git
- Jenkins with Plugins (Git plugin, Maven Integration plugin, JUnit plugin)
Theory:
What is Continuous Testing?
Continuous Testing is a process where automated tests are integrated into the software delivery pipeline
to validate the quality of applications at each step. This ensures faster feedback and quicker release cycles in DevOps
Algorithm:
Step 1: Install Prerequisites
- Install Java, Maven, and Git.
- Download and install Jenkins.
- Install required Jenkins plugins: Git plugin, Maven Integration plugin, JUnit plugin
Step 2: Create a Sample Maven Project
Structure:
sample-app/
|-- src/
| |-- main/
| | `-- java/
| |-- test/
| `-- java/
| `-- TestCalculator.java
|-- pom.xml
Step 3: Implement Sample Code (Calculator.java)
public class Calculator {
public int add(int a, int b) { return a + b; }
public int subtract(int a, int b) { return a - b; }
}
Step 4: Create JUnit Test (TestCalculator.java)
import org.junit.Test;
import static org.junit.Assert.*;
public class TestCalculator {
@Test public void testAddition() {
Calculator calc = new Calculator();
assertEquals(10, calc.add(5, 5));
}
@Test public void testSubtraction() {
Calculator calc = new Calculator();
assertEquals(3, calc.subtract(5, 2));
}
}
Step 5: Configure Maven (pom.xml)
<dependencies>
<dependency>
<groupId>junit</groupId>
<artifactId>junit</artifactId>
<version>4.13.2</version>
<scope>test</scope>
</dependency>
</dependencies>
Step 6: Initialize Git Repository
git init
git add .
git commit -m "Initial project with tests"
Step 7: Setup Jenkins Job for Continuous Testing
- Open Jenkins at: http://localhost:8080
- Create Freestyle Project: SampleApp-CI
- Link to Git repository, enable Poll SCM (H/5 * * * *)
- Add Build Step: mvn clean test
- Add Post-build Action: Publish JUnit report (target/surefire-reports/*.xml)
Step 8: Commit and Push Changes
git add .
git commit -m "Add continuous testing"
git push origin main
Step 9: Observe Results in Jenkins
- Check Build History, Console Output, and Test Results tab.
Result:
The experiment was successfully completed. Continuous Testing was implemented using Jenkins, Git, and Maven in Observation Table:
| Step | Observation |
|-------------------|-------------------------------------|
| Install Tools | Java, Maven, Git, Jenkins installed |
| Project Creation | Maven project created |
| Git Initialized | Repository initialized in Git |
| Jenkins Job | Jenkins job configured |
| Trigger & Observe | Build triggered, tests executed |
| Result Observed | Test results displayed in Jenkins |
Conclusion:
This experiment demonstrated Continuous Testing in the DevOps lifecycle using Jenkins and Maven, ensuring continuous Advantages:
- Early defect detection.
- Automated test execution.
- Reduces manual testing.
- Faster developer feedback.
Applications:
- Used in DevOps pipelines.
- Applied in CI/CD.
- Supports Agile teams.
- Ensures production-ready quality.

Experiment No- 4
AIM:
To explore and practice basic Git and GitHub commands.
OBJECTIVES:
Understand version control concepts.
Learn basic Git commands for local repository management.
Explore GitHub for remote repository handling.
MATERIALS REQUIRED:
A computer with Git installed.
A GitHub account.
Internet connection.
THEORY:
Git is a distributed version control system used for tracking changes in source code during software development. GitHub is a cloud-based hosting service that helps developers manage Git repositories collaboratively.
PROCEDURE:
Step 1: Install Git
Check if Git is installed:
git --version
If not installed, download and install Git from https://git-scm.com/.
Step 2: Configure Git
Set up user information:
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
Step 3: Initialize a Local Repository
Create a new directory and navigate into it:
mkdir my-project
cd my-project
Initialize Git:
git init
Step 4: Create and Commit Files
Create a new file:
echo "Hello, Git!" > README.md
Add the file to staging:
git add README.md
Commit the changes:
git commit -m "Initial commit"
Step 5: Connect to GitHub
Create a new repository on GitHub (without initializing README).
Add the remote repository:
git remote add origin https://github.com/your-username/my-project.git
Step 6: Push Changes to GitHub
Push the local commits to GitHub:
git branch -M main
git push -u origin main
Step 7: Clone a Repository
Clone a GitHub repository:
git clone https://github.com/your-username/my-project.git
Step 8: Pull and Fetch Changes
Fetch the latest changes from the remote repository:
git fetch
Pull changes into your local repository:
git pull origin main
Step 9: Branching and Merging
Create a new branch:
git branch feature-branch
Switch to the new branch:
git checkout feature-branch
Merge the branch:
git checkout main
git merge feature-branch
Step 10: Undoing Changes
Revert the last commit:
git revert HEAD
Reset to a previous state:
git reset --hard <commit-hash>
OBSERVATIONS:
Noted how Git tracks changes in files.
Understood the role of GitHub in collaboration.
Learned different Git commands for version control.
CONCLUSION:
This experiment helped in understanding the fundamental Git and GitHub commands used in version control and collaborative development.





















Experiment No- 5
AIM:
Creating a New Git Repository and Pushing Changes to a Remote Repository

Objective:
 To understand and implement the process of creating a Git repository, adding a README file, committing changes, and pushing them to a remote repository.
Requirements:
Git installed on your system
A GitHub account
Internet connection
Algorithm:
Initialize a Git Repository:
Open the terminal or command prompt.
Navigate to the desired directory where you want to create the repository.
Run the following command to initialize the repository:
      git init
Create a README File:
Use the following command to create a README file:
echo "# My New Repository" > README.md
Alternatively, create the file manually and add some content.
Add the README File to Staging Area:
Use the following command to add the file to the staging area:
git add README.md
Commit the Changes:
Commit the added file using the following command:
git commit -m "Initial commit: Added README file"
Create a Remote Repository on GitHub:
Log in to your GitHub account.
Click on the "+" icon and select "New repository".
Enter a repository name and description.
Choose "Public" or "Private" as per requirement.
Click "Create repository".
Link the Local Repository to Remote Repository:
Copy the repository URL from GitHub.
Run the following command to add the remote origin:
git remote add origin <repository_url>
Push the Changes to Remote Repository:
Use the following command to push the changes:
git push -u origin main
If the default branch is "master", use:
git push -u origin master
Verification:
Go to your GitHub repository page and verify that the README file has been uploaded successfully.
Conclusion: By following these steps, we successfully created a Git repository, added a README file, committed the changes, and pushed them to a remote repository on GitHub.




Experiment No- 6
AIM:
Create a new branch called "MITS" and make some changes to a file. Commit the changes and merge the branch with the main branch.
	
 Objective:
To understand the process of creating a new branch in Git, making changes to a file, committing those changes, and merging the branch back into the main branch.
Requirements:
Git installed on the system
A working terminal or command prompt

Procedure:

Step 1: Initialize a Git Repository
```bash
git init
```
This command initializes a new Git repository in the current directory.

Step 2: Create a New Branch
```bash
git checkout -b MITS
```
This command creates a new branch named "MITS" and switches to it.

Step 3: Make Changes to a File
```bash
echo "This is a test change in the MITS branch." > sample.txt
```
This command creates a new file named `sample.txt` and writes some content into it.

Step 4: Add and Commit the Changes
```bash
git add sample.txt
git commit -m "Added sample.txt with initial content in MITS branch"
```
These commands stage and commit the changes made to `sample.txt`.

Step 5: Switch Back to the Main Branch
Experiment No- 4
AIM:
To explore and practice basic Git and GitHub commands.
OBJECTIVES:
Understand version control concepts.
Learn basic Git commands for local repository management.
Explore GitHub for remote repository handling.
MATERIALS REQUIRED:
A computer with Git installed.
A GitHub account.
Internet connection.
THEORY:
Git is a distributed version control system used for tracking changes in source code during software development. GitHub is a cloud-based hosting service that helps developers manage Git repositories collaboratively.
PROCEDURE:
Step 1: Install Git
Check if Git is installed:
git --version
If not installed, download and install Git from https://git-scm.com/.
Step 2: Configure Git
Set up user information:
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
Step 3: Initialize a Local Repository
Create a new directory and navigate into it:
mkdir my-project
cd my-project
Initialize Git:
git init
Step 4: Create and Commit Files
Create a new file:
echo "Hello, Git!" > README.md
Add the file to staging:
git add README.md
Commit the changes:
git commit -m "Initial commit"
Step 5: Connect to GitHub
Create a new repository on GitHub (without initializing README).
Add the remote repository:
git remote add origin https://github.com/your-username/my-project.git
Step 6: Push Changes to GitHub
Push the local commits to GitHub:
git branch -M main
git push -u origin main
Step 7: Clone a Repository
Clone a GitHub repository:
git clone https://github.com/your-username/my-project.git
Step 8: Pull and Fetch Changes
Fetch the latest changes from the remote repository:
git fetch
Pull changes into your local repository:
git pull origin main
Step 9: Branching and Merging
Create a new branch:
git branch feature-branch
Switch to the new branch:
git checkout feature-branch
Merge the branch:
git checkout main
git merge feature-branch
Step 10: Undoing Changes
Revert the last commit:
git revert HEAD
Reset to a previous state:
git reset --hard <commit-hash>
OBSERVATIONS:
Noted how Git tracks changes in files.
Understood the role of GitHub in collaboration.
Learned different Git commands for version control.
CONCLUSION:
This experiment helped in understanding the fundamental Git and GitHub commands used in version control and collaborative development.





















Experiment No- 5
AIM:
Creating a New Git Repository and Pushing Changes to a Remote Repository

Objective:
 To understand and implement the process of creating a Git repository, adding a README file, committing changes, and pushing them to a remote repository.
Requirements:
Git installed on your system
A GitHub account
Internet connection
Algorithm:
Initialize a Git Repository:
Open the terminal or command prompt.
Navigate to the desired directory where you want to create the repository.
Run the following command to initialize the repository:
      git init
Create a README File:
Use the following command to create a README file:
echo "# My New Repository" > README.md
Alternatively, create the file manually and add some content.
Add the README File to Staging Area:
Use the following command to add the file to the staging area:
git add README.md
Commit the Changes:
Commit the added file using the following command:
git commit -m "Initial commit: Added README file"
Create a Remote Repository on GitHub:
Log in to your GitHub account.
Click on the "+" icon and select "New repository".
Enter a repository name and description.
Choose "Public" or "Private" as per requirement.
Click "Create repository".
Link the Local Repository to Remote Repository:
Copy the repository URL from GitHub.
Run the following command to add the remote origin:
git remote add origin <repository_url>
Push the Changes to Remote Repository:
Use the following command to push the changes:
git push -u origin main
If the default branch is "master", use:
git push -u origin master
Verification:
Go to your GitHub repository page and verify that the README file has been uploaded successfully.
Conclusion: By following these steps, we successfully created a Git repository, added a README file, committed the changes, and pushed them to a remote repository on GitHub.




Experiment No- 6
AIM:
Create a new branch called "MITS" and make some changes to a file. Commit the changes and merge the branch with the main branch.
	
 Objective:
To understand the process of creating a new branch in Git, making changes to a file, committing those changes, and merging the branch back into the main branch.
Requirements:
Git installed on the system
A working terminal or command prompt

Procedure:

Step 1: Initialize a Git Repository
```bash
git init
```
This command initializes a new Git repository in the current directory.

Step 2: Create a New Branch
```bash
git checkout -b MITS
```
This command creates a new branch named "MITS" and switches to it.

Step 3: Make Changes to a File
```bash
echo "This is a test change in the MITS branch." > sample.txt
```
This command creates a new file named `sample.txt` and writes some content into it.

Step 4: Add and Commit the Changes
```bash
git add sample.txt
git commit -m "Added sample.txt with initial content in MITS branch"
```
These commands stage and commit the changes made to `sample.txt`.

Step 5: Switch Back to the Main Branch
```bash
git checkout main
```
This command switches back to the main branch.

Step 6: Merge the MITS Branch with the Main Branch
```bash
git merge MITS
```
This command merges the `MITS` branch into the `main` branch.

Step 7: Delete the MITS Branch (Optional)
```bash
git branch -d MITS
```
This command deletes the `MITS` branch after merging.

Expected Output:
- A new branch `MITS` is created.
- Changes are made to `sample.txt`.
- The changes are committed and merged back into the `main` branch.
- The `MITS` branch is deleted after merging.

Conclusion:
This experiment demonstrates the fundamental operations of branching, modifying files, committing changes, and merging branches in Git, which are essential for version control in software development.







Experiment No-7
AIM:
Use Git log to view the commit history of a repository and find the commit hash of a specific commit.

Objective: 
To understand how to use git log to view the commit history of a Git repository and retrieve the commit hash of a specific commit.
Requirements:
A computer with Git installed
A pre-existing Git repository or a newly initialized repository
Basic knowledge of Git commands
Procedure:
Setting Up the Environment:
Open a terminal (Command Prompt, Git Bash, or Terminal).
Navigate to the repository using the cd command.
cd path/to/your/repository
Viewing the Commit History:
Use the git log command to display the commit history.
git log
This command will show the commit history with details like commit hash, author, date, and commit message.
Finding a Specific Commit Hash:
Scroll through the commit history and locate the commit message corresponding to the commit of interest.
The commit hash is the long alphanumeric string at the beginning of each commit entry.
Filtering the Commit History:
Use the --oneline option to display a simplified history.
git log --oneline
This shows only the commit hashes and messages in a single line per commit.
Example output:
a1b2c3d Update README file
e4f5g6h Fix login bug
i7j8k9l Initial commit
Identify the hash of the required commit from this output.
Searching for a Specific Commit Message:
Use git log --grep="commit message" to search for a commit by message.
git log --grep="Fix login bug"
Viewing Commit Details Using Commit Hash:
Once the commit hash is identified, use it to view detailed information about the commit.
git show a1b2c3d
Observations:
The commit history provides a chronological view of repository changes.
The commit hash uniquely identifies each commit.
Filtering options help quickly locate a specific commit.









Experiment No- 8
AIM:
Cloning a Git Repository from a Remote Repositor

Objective: To understand and perform the process of cloning a Git repository from a remote repository using Git commands.
Prerequisites:
Basic understanding of Git and version control.
Git installed on the system.
An active internet connection.
A GitHub, GitLab, or Bitbucket account.
Materials Required:
A computer with Git installed.
A pre-existing repository URL from a remote platform (GitHub, GitLab, etc.).
Step 1: Verify Git Installation
Step 1: Verify Git Installation
Open the terminal or command prompt.
Run the following command to check if Git is installed:
git --version
If Git is not installed, download and install it from Git Official Website.
Step 2: Navigate to the Desired Directory
Choose a directory where you want to clone the repository.
Use the cd command to navigate to that directory:
cd path/to/your/directory
Step 3: Clone the Repository
Copy the repository URL from the remote platform (GitHub, GitLab, etc.).
Run the following command to clone the repository:
git clone <repository_url>
Example:
git clone https://github.com/example-user/example-repo.git
This command downloads the repository to your local system.
Step 4: Verify Cloning
Navigate into the cloned repository:
cd example-repo
List the files to check the contents:
ls  (Linux/macOS)
dir (Windows)
Check the remote repository link:
git remote -v
Step 5: Make a Change and Push to Remote (Optional)
Create a new file inside the cloned repository:
echo "Hello Git" > testfile.txt
Add the file to the staging area:
git add testfile.txt
Commit the changes:
git commit -m "Added testfile.txt"
Push the changes to the remote repository:
git push origin main

Expected Outcome: Students should be able to successfully clone a Git repository, navigate within it, and optionally make changes and push updates to the remote repository.



Experiment No- 9
AIM:
Pushing Changes from Local Repository to Remote Repository Using Git.
Objective: To understand and perform the process of pushing local repository changes to a remote repository using Git.
Prerequisites:
Basic knowledge of Git and GitHub.
Git installed on the system.
A GitHub account.
Software & Tools Required:
Git
GitHub
Command Line Interface (CLI) or Git Bash
Theory: Version control systems help track changes in code over time. Git is a distributed version control system that allows multiple developers to work collaboratively. Pushing changes means transferring committed changes from a local repository to a remote repository.
Experimental Setup:
Install Git (if not installed):
Windows: Download from https://git-scm.com/ and install.
Linux: Use sudo apt install git (Debian-based) or sudo yum install git (RHEL-based).
MacOS: Use brew install git.
Set Up Git (First-time users)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
Procedure:
Create a Local Repository
mkdir MyProject
cd MyProject
git init
This initializes a new Git repository in the MyProject directory.
Create a File and Make Initial Commit
echo "Hello, Git!" > file.txt
git add file.txt
git commit -m "Initial commit"
This creates a file, adds it to the staging area, and commits it.
Create a Remote Repository on GitHub
Log in to GitHub and create a new repository.
Copy the repository URL.
Connect Local Repository to Remote Repository
git remote add origin <repository_URL>
Push Changes to Remote Repository
git branch -M main
git push -u origin main
This pushes the committed changes to the remote repository.	


Expected Output:
A new repository is created on GitHub with the committed file.
The repository reflects the changes made locally.





Experiment No- 10
AIM:
Inspecting a Web Element in Google Homepage Using Selenium in Edge Browser
Objective: To understand and implement Selenium WebDriver to open Microsoft Edge, navigate to Google’s homepage, and inspect a web element.
Requirements:
Python installed on the system
Microsoft Edge browser
Edge WebDriver (compatible with your Edge version)
Selenium library installed (pip install selenium)
Theory: Selenium is an open-source automation tool used for testing web applications. It supports multiple programming languages and browsers. Web elements on a webpage can be identified using various locators such as ID, Name, XPath, and CSS Selector.
Steps to Perform:
Setup Environment:
Install Python and ensure it is added to the system PATH.
Install Selenium using:
pip install selenium
Download the Edge WebDriver from Microsoft Edge WebDriver and place it in a known directory.
Write a Python Script:
Open a text editor or IDE and write the following script:
from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# Set up Edge WebDriver path
driver = webdriver.Edge(executable_path="path_to_msedge_driver")

# Open Google homepage
driver.get("https://www.google.com")
time.sleep(2)

# Inspect the search box element
search_box = driver.find_element(By.NAME, "q")
print("Search box element found:", search_box)

# Close the browser
driver.quit()
Run the Script:
Replace path_to_msedge_driver with the actual path of your Edge WebDriver.
Save the script as selenium_test.py and run it using:
python selenium_test.py
The script will open the Edge browser, navigate to Google, identify the search box, and print details about it.
Observations:
The script should launch the browser and navigate to Google.
It should locate the search box element and print its details.
The browser should close after execution.
Result: Students will successfully automate the process of inspecting a web element in Google using Selenium with Edge.


Experiment No- 11
AIM:	
Automating Facebook Login using Selenium
Objective:
To automate the login process of Facebook using Selenium WebDriver in Python and display the homepage.

Requirements:
Python installed on the system.
Selenium library installed (pip install selenium).
WebDriver (ChromeDriver/EdgeDriver) installed.
Microsoft Edge browser installed.
A valid Facebook account for testing.

Procedure:
Step 1: Install Selenium	
Ensure that Selenium is installed by running the following command:
pip install selenium
Step 2: Download Edge WebDriver
Download the Edge WebDriver compatible with your browser version from:
https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
Place the WebDriver in a known directory (e.g., C:\WebDriver\msedgedriver.exe).
Step 3: Write the Python Script
Create a new Python script (facebook_login.py) and add the following code:
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

# Set up Edge WebDriver
EDGE_DRIVER_PATH = "C:\\WebDriver\\msedgedriver.exe"
options = webdriver.EdgeOptions()
driver = webdriver.Edge(executable_path=EDGE_DRIVER_PATH, options=options)

# Open Facebook Login Page
driver.get("https://www.facebook.com/")
time.sleep(3)  # Allow page to load

# Locate the email and password fields
email_field = driver.find_element(By.ID, "email")
password_field = driver.find_element(By.ID, "pass")
login_button = driver.find_element(By.NAME, "login")

# Enter credentials
email_field.send_keys("your_email@example.com")  # Replace with your email
password_field.send_keys("your_password")  # Replace with your password

# Click login
login_button.click()
time.sleep(5)  # Wait for login process

# Verify login success by checking homepage URL
if "facebook.com" in driver.current_url:
    print("Login successful! Facebook homepage loaded.")
else:
    print("Login failed. Check credentials.")

# Close the browser
driver.quit()
Step 4: Run the Script
Execute the script by running:
python facebook_login.py
Observations:
The browser should open and navigate to Facebook.
Credentials should be entered automatically.
If login is successful, the Facebook homepage should be displayed.
The script prints a success or failure message.












Experiment No- 12
AIM:
Testing Web Elements on Google Homepage Using Selenium


Objective: To automate web testing using Selenium by identifying and interacting with web elements on the Google homepage.
Requirements:
Python (latest version)
Selenium WebDriver
Microsoft Edge Browser and Edge WebDriver
Installation Steps:
Install Selenium using pip:
pip install selenium
Download and set up Microsoft Edge WebDriver compatible with your browser version from: https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
Ensure the WebDriver executable is placed in a directory included in the system PATH.
Experiment Steps:
Import Required Modules:
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
            import time
Launch Microsoft Edge and Open Google Homepage:
driver = webdriver.Edge()
driver.get("https://www.google.com")
            driver.maximize_window()
Identify and Test Web Elements:
Google Search Box:
search_box = driver.find_element(By.NAME, "q")
search_box.send_keys("Selenium Web Testing")
search_box.send_keys(Keys.RETURN) time.sleep(3)
Google Search Button (Optional as pressing RETURN in search box works):
search_button = driver.find_element(By.NAME, "btnK")
print("Google Search button found.")
Google Apps Button:
apps_button = driver.find_element(By.CLASS_NAME, "gb_D")
print("Google Apps button located.")
Sign-in Button:
sign_in_button = driver.find_element(By.LINK_TEXT, "Sign in")
print("Sign-in button located.")
Footer Elements:
footer_links = driver.find_elements(By.TAG_NAME, "a")
for link in footer_links:
    	print(link.text, "->", link.get_attribute("href"))
Close the Browser:
driver.quit()
Expected Outcome: 
Open the Google homepage in the Edge browser.
Identify and interact with web elements using Selenium.
Automate a simple Google search.
Extract and print footer links.



Experiment No- 13
AIM:	
Lab Experiment: Basic Docker Commands


Objective: 
To understand and execute fundamental Docker commands for containerization, image management, and container lifecycle operations.
Prerequisites:
Basic knowledge of Linux commands
Docker installed on the system
Lab Setup:
Ensure that Docker is installed by running:
docker --version
Experiment Steps:
Step 1: Verify Docker Installation
Run the following command to check if Docker is installed correctly:
docker --version
Output example:
Docker version 20.10.12, build e91ed57
Step 2: Pull an Image from Docker Hub
Download an official image (e.g., Ubuntu) from Docker Hub:
docker pull ubuntu
Verify the downloaded image:
docker images
Step 3: Run a Container
Start a container from the Ubuntu image:
docker run -it ubuntu
This command starts an interactive shell inside the container. Exit the container using:
exit
Step 4: List Running Containers
To view active containers:
docker ps
To view all containers (including stopped ones):
docker ps -a
Step 5: Restart and Stop a Container
Find the container ID using docker ps -a and use it to restart:
docker start <container_id>
Stop the container:
docker stop <container_id>
Step 6: Remove a Container and Image
Remove a stopped container:
docker rm <container_id>
Remove an image:
docker rmi ubuntu
Step 7: Create and Use a Dockerfile
Create a file named Dockerfile and add the following content:
FROM ubuntu
RUN apt-get update && apt-get install -y curl
CMD ["echo", "Hello, Docker!"]
Build the image:
docker build -t mycustomimage .
Run the container:
docker run mycustomimage
Expected output:
Hello, Docker!
Conclusion: This lab introduced basic Docker commands for managing containers and images. Students should now be able to perform fundamental operations in Docker.




















































Experiment No- 14
AIM:	
Deploying a Simple HTML Webpage using Docker

Objective: To understand and implement Docker containerization by deploying a simple HTML webpage using Docker.
Prerequisites:
Basic knowledge of HTML and Docker
Docker installed on the system
Experiment Steps:
Step 1: Create a Simple HTML File
Open a text editor and create a new file named index.html.
Add the following HTML content:
<!DOCTYPE html>
<html>
<head>
    <title>Hello, World!</title>
</head>
<body>
    <h1>Hello, World!</h1>
</body>
</html>
Save the file in a new directory (e.g., docker-webpage).
Step 2: Create a Dockerfile
In the same directory, create a file named Dockerfile (without any extension).
Add the following content to the Dockerfile:
# Use an official Nginx image as the base image
FROM nginx:latest

# Copy the HTML file to the Nginx default directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80
EXPOSE 80
Save the file.
Step 3: Build the Docker Image
Open a terminal or command prompt and navigate to the docker-webpage directory.
Run the following command to build the Docker image:
docker build -t my-html-app .
Step 4: Run the Docker Container
Use the following command to start a container from the built image:
docker run -d -p 8080:80 my-html-app
This maps port 80 of the container to port 8080 of the local machine.
Step 5: View the Webpage
Open a web browser and enter the following URL:
http://localhost:8080
You should see the message "Hello, World!" displayed.
Step 6: Stop and Remove the Container (Optional)
To stop the container, run:
docker ps   # To find the running container ID
docker stop <container_id>
To remove the container, run:
docker rm <container_id>
Conclusion: 
In this lab, we successfully built and ran a Docker container to serve a simple HTML webpage using Nginx. This experiment demonstrates the power of containerization in deploying web applications efficiently.






































Experiment No- 15
AIM:	
Building a Docker Image Based on Alpine with Nano Installed


Objective: 
To build a Docker image using the official Alpine Linux image that includes the Nano text editor and to verify its functionality by running a container.
Prerequisites:
A system with Docker installed.
Basic understanding of Docker commands.
Internet connectivity to pull the Alpine image.

Step 1: Create a Dockerfile
Create a new directory for the project and navigate into it:
mkdir alpine-nano && cd alpine-nano
Create a Dockerfile inside this directory and add the following content:
# Use the official Alpine image as base
FROM alpine:latest

# Install Nano text editor
RUN apk add --no-cache nano

# Set the default command to launch a shell
CMD ["/bin/sh"]
Save and close the file.

Step 2: Build the Docker Image
Run the following command to build the Docker image:
docker build -t alpine-nano .
This command:
Downloads the latest Alpine Linux image.
Installs Nano.
Tags the image as alpine-nano.

Step 3: Run a Container from the Image
Start a container using the newly built image:
docker run -it --name nano-container alpine-nano
This command:
Runs the container interactively (-it).
Names the container nano-container.
Uses the alpine-nano image.
Once inside the container, verify that Nano is installed:
nano --version
If installed correctly, it should display the Nano version information.

Step 4: Test Nano
Inside the container, create and open a new file with Nano:
nano testfile.txt
Type some text into the file.
Save and exit Nano by pressing CTRL + X, then Y, and Enter.
Verify that the file exists:
cat testfile.txt

Step 5: Exit and Cleanup
Exit the container:
exit
Remove the container (optional):
docker rm nano-container
Remove the image (optional):
docker rmi alpine-nano

Conclusion: In this experiment, we successfully created a Docker image using Alpine Linux with Nano installed, ran a container from the image, and verified that Nano was functional.




















































Experiment No- 16
AIM:	
Running MySQL in Docker and Executing Queries

Objective: To learn how to set up and run a MySQL container using Docker and execute basic SQL queries.

Prerequisites:
Basic understanding of Docker and MySQL
Docker installed on your system

Step 1: Pulling the MySQL Docker Image
Open the terminal and run the following command to pull the official MySQL image:
docker pull mysql:latest
Verify the image is downloaded using:
docker images

Step 2: Running a MySQL Container
Start a MySQL container with the following command:
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -d mysql:latest
--name mysql-container: Assigns a name to the container.
-e MYSQL_ROOT_PASSWORD=root: Sets the root password.
-d: Runs the container in detached mode.
Verify the container is running:
docker ps

Step 3: Connecting to MySQL Container
Access the MySQL container:
docker exec -it mysql-container mysql -uroot -proot
-it: Interactive mode
mysql -uroot -proot: Logs into MySQL using the root credentials.
Check the existing databases:
SHOW DATABASES;

Step 4: Creating a Database and Table
Create a new database:
CREATE DATABASE student_db;
Switch to the newly created database:
USE student_db;
Create a table:
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
Verify the table creation:
SHOW TABLES;

Step 5: Inserting and Querying Data
Insert a record into the table:
INSERT INTO students (name, age) VALUES ('John Doe', 22);
Retrieve all records:
SELECT * FROM students;

Step 6: Stopping and Removing the Container
Stop the running MySQL container:
docker stop mysql-container
Remove the container:
docker rm mysql-container
Remove the MySQL image if needed:
docker rmi mysql:latest

Expected Output:
Successful execution of MySQL queries inside a Docker container.
Proper understanding of Docker container lifecycle.































Experiment No- 17
AIM:	
Deploying MySQL with phpMyAdmin using Docker

Prerequisites:
Basic knowledge of Docker
Installed Docker on your system
Experiment Steps:
Step 1: Install Docker
Ensure Docker is installed on your system. You can check the installation using:
 docker --version
If not installed, download and install it from Docker Official Site.
Step 2: Create a Docker Network
Docker network allows containers to communicate with each other.
docker network create mynetwork
Step 3: Pull MySQL Image and Run a Container
Run the following command to pull and start a MySQL container:
docker run --name mysql-container --network mynetwork -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=mydb -d mysql:latest
--name mysql-container assigns a name to the container.
--network mynetwork connects the container to our created network.
-e MYSQL_ROOT_PASSWORD=root sets the root password.
-e MYSQL_DATABASE=mydb creates a default database.
-d mysql:latest runs the container in detached mode using the latest MySQL image.
Step 4: Deploy phpMyAdmin Container
Run the following command to deploy phpMyAdmin:
docker run --name phpmyadmin-container --network mynetwork -d -e PMA_HOST=mysql-container -p 8080:80 phpmyadmin/phpmyadmin
--name phpmyadmin-container assigns a name to the phpMyAdmin container.
--network mynetwork connects it to the same network as MySQL.
-e PMA_HOST=mysql-container links phpMyAdmin with MySQL.
-p 8080:80 maps port 8080 of the host to port 80 of the container.
-d phpmyadmin/phpmyadmin runs the latest phpMyAdmin image in detached mode.
Step 5: Access phpMyAdmin
Open a web browser and navigate to: http://localhost:8080
Login using:
Username: root
Password: root
You should now see the mydb database in phpMyAdmin.
Step 6: Create a Table in MySQL
After logging into phpMyAdmin:
Select mydb from the left panel.
Click on SQL and execute the following query to create a table:
CREATE TABLE students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    age INT
);


Step 7: Insert Data into the Table
Execute the following SQL query to insert data:
INSERT INTO students (name, age) VALUES ('Alice', 21), ('Bob', 22);
Step 8: Retrieve Data
Execute the query to fetch all records:
SELECT * FROM students;
Step 9: Stopping and Removing Containers
To stop and remove the containers, run:
docker stop mysql-container phpmyadmin-container
docker rm mysql-container phpmyadmin-container
docker network rm mynetwork

Conclusion:
By completing this experiment, students have learned how to:
Pull and run MySQL and phpMyAdmin using Docker.
Create a database and a table using phpMyAdmin.
Insert and retrieve data using SQL queries.
