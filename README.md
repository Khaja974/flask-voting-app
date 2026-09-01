# flask-voting-app
Hero vired Flask Assignment
Flask Voting Application – Khaja Nawaz Shaik Project Documentation
This documentation is prepared based on the Flask Application with Git Versioning Workflow assignment. It provides the content to use in the project's README.md file.
1. Project Title and Description
The Flask Voting Application is a simple web application that allows users to vote for candidates through web URLs. Each vote is recorded and the application keeps track of the total votes for each candidate. Users can view the current voting results and, in Version 2, reset all stored votes.
2. Features
•	Welcome page
•	Application health check
•	Vote for a candidate
•	View current voting results
•	Reset all votes
•	In-memory vote storage using a Python dictionary
•	Git version control using dev and main branches
3. Technologies Used
•	Python 3.x
•	Flask
•	Git
•	GitHub
•	VS Code
4. Installation and Setup
Clone the Repository
git clone  https://github.com/Khaja974/flask-voting-app.git
cd flask-voting-app
Create a Virtual Environment
python -m venv venv
Windows: venv\Scripts\activate
Install Dependencies
pip install 
Run the Application
python app.py
The application should be available at: http://localhost:5000
5. API Endpoint Reference
Version	Endpoint	Method	Description	Example Response
V1	/	GET	Displays the welcome message	Welcome to the App
V1	/health	GET	Checks whether the application is running	App is running
V1	/vote/<name>	GET	Records one vote for the specified candidate	{"candidate":"Nawaz","votes":1}
V1	/results	GET	Returns current vote counts as JSON	{"Nawaz":2,"Shaik":1}
V2	/reset	GET	Clears all stored vote counts	{"message":"All votes have been reset"}
6. API Usage Examples
/
URL: http://localhost:5000/
Example response: Welcome to the App
/health
URL: http://localhost:5000/health
Example response: App is running
/vote/Alice
URL: http://localhost:5000/vote/Alice
Example response: {"candidate":"Nawaz","votes":1}
/results
URL: http://localhost:5000/results
Example response: {"Nawaz":2,"Shaik":1, ,"Khaja":2}
/reset
URL: http://localhost:5000/reset
Example response: {"message":"All votes have been reset"}
7. How the Voting System Works
The application stores vote counts in memory using a Python dictionary. When a new candidate receives a vote, their count starts at 1. If the candidate already exists, the count increases by 1. The /results endpoint returns the current vote counts as JSON. Because the data is stored in memory, it is cleared when the application is stopped or restarted.
8. Git Workflow
The project uses two Git branches: dev and main. Development and testing are performed in the dev branch. After a version is complete and working, dev is merged into main. The main branch therefore contains stable code.
Development flow:
dev → development/testing → commit → push dev → merge dev into main → push main
Version 1 Git Workflow
git init
git checkout -b dev
git add .
git commit -m "feat: implement version 1 voting application"
git push origin dev
git checkout main
git merge dev
git push origin main
Version 2 Git Workflow
git checkout dev
git add .
git commit -m "feat: add reset votes endpoint"
git push origin dev
git checkout main
git merge dev
git push origin main
9. Version History
Version	Features
Version 1	Basic Flask application, /, /health, /vote/<name>, and /results
Version 2	Added /reset endpoint to clear all stored votes
10. Project Structure
flask-voting-app/
├── app.py
├── requirements.txt
├── README.md
├── venv/
└── images/
    ├── git-init.png 
    ├── created-readme.png 
   ├── vote-entry.png 
   ├── first-result.png 
   ├── first-git-commit.png 
  ├── created-dev-branch.png 
  ├── created-dev-branch-on-github.png 
  ├── version2-added-vote-entry.png 
  ├── version2-git-commit.png 
  ├── version2-git-push-dev.png 
  ├── version2-git-push-origin-main.png 
  ├── version2-vote-results.png 
  ├── version2-reset-run.png 
  ├── version2-after-reset-result.png 
  ├── vote-results-1.png 
  └── vote-results-2.png 
11. Screenshots Required in README.md
•	Application running in a browser showing at least one working endpoint.
•	GitHub repository page showing both the dev and main branches.
•	Commit or merge history showing the Version 1 and Version 2 releases.
After taking the screenshots, save them inside the screenshots folder and embed them in README.md using Markdown, for example:
12. Final Checklist
•	Flask application runs successfully on localhost.
•	The / endpoint returns 'Welcome to the App'.
•	The /health endpoint returns 'App is running'.
•	The /vote/<name> endpoint records and increments votes.
•	The /results endpoint returns vote counts in JSON format.
•	The /reset endpoint clears all votes.
•	Git repository contains dev and main branches.
•	Version 1 is merged from dev into main.
•	Version 2 is developed in dev and merged into main.
•	README.md contains all required sections.
•	All three required screenshots are embedded in README.md.
