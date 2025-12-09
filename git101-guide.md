
# 🧠 git Commands

## 🎯 Create New Directory
      1. Go to to root directory: c~ + enter.
      2. Create new directory: $ mkdir "myWorkspace - Bookstore" + enter.
      3. Go to your workspace: $ cd + workspace path + enter.
      4. View current directory: pwd
      5. View files and sub-directory: dir
      6. View directory: ls + enter
      7. View directory with hidden files: ls -a + enter</li>

---

## ✍️ Clone Repo
    1. Get Repo URL from gitHub:
        - Open github
        - Expand Code menu
        - Copy URL

    2. Clone Repo - copy the remote repository to your local machine:
        - Open Command Prompt and Navigate to Directory: C:\> cd "myWorkspace - Bookstore" 
        - Type git clone + URL and hit Enter 
        - Type C:\myWorkspace - Bookstore> cd + repoName (e.g .\automation-bookstore\) 
        - Type C:\>code . to open VSCode 
        - Copy URL 

## ✍️ Update and Commit to gitHub
    1. Type Ctrl+` to open VSCode Terminal 
    2. Type C:\...\automation-bookstore> git status to confirm status of current branch 
    3. Type C:\...\automation-bookstore> git add fileName or git add . to add ALL changes. Use git status to confirm 
    4. Type C:\...\automation-bookstore> git commit -m initialcommit to commit changes 
    5. Type C:\...\automation-bookstore> git push origin [branchName e.g. main] to add changes to Repo 
---
## ✍️ Update and Commit to gitHub
    1. Type C:\...\automation-bookstore> git status to confirm status of current branch 
    2. Type C:\...\automation-bookstore> git commit -m initialcommit to commit changes 
    5. Type C:\...\automation-bookstore> git push origin [branchName e.g. master] to add changes to Repo 
---

## ✅ Example: Login Functionality
Feature: User Login

Scenario: Successful login with valid credentials  
Given the user is on the login page When the user enters valid username and password  
And clicks the login button  
Then the user should be redirected to the dashboard  

Scenario: Login fails with invalid credentials  
Given the user is on the login page  
When the user enters invalid username or password  
And clicks the login button  
Then an error message should be displayed  

---

## 💡 Tips for Writing Gherkin

| Tip | Description |
|-----|-------------|
| Use plain language | Avoid technical jargon |
| Be specific | Define clear inputs and expected outcomes |
| Keep it atomic | One scenario = one test case |
| Reuse steps | Common steps can be reused across scenarios |
| Focus on behavior | Describe what the system should do, not how |

---

## 🧩 Mapping to Automation

Each Gherkin step is mapped to a Java method using annotations:

```java
public class ExampleFeature{
    @Given("the user is on the login page")
    public void navigateToLoginPage() {
        loginPage.open();
    }
}
```

---

## 📌 Where to Place Gherkin Files
Place .feature files under:  src/test/resources/features/

---
##🤝 Collaboration Workflow
1. Business Analyst writes Gherkin scenarios.  
2. QA Engineer maps steps to automation code.  
3. Developer ensures feature implementation aligns with scenarios.  
4. Test Execution validates behavior against expectations.

##📎 Resources
1. [Cucumber Reference](https://cucumber.io/docs/guides/10-minute-tutorial/) 
2. [Gherkin Syntax Cheatsheet](https://cucumber.io/docs/gherkin/reference/)