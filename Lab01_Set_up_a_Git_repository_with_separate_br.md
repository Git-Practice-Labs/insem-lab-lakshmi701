# Lab 01: Set up a Git repository with separate branches for frontend and backend, then merge them into the main branch.

## Objective
To learn how to create a Git repository, make separate branches for frontend and backend, and merge them into the main branch.

## Tools / Technologies
Git
GitHub
Git Bash / VS Code

## Prerequisites
Git installed
GitHub account
Internet connection

## Steps / Commands
1.Initialize Repository
    mkdir Lab01_GitSetup
    cd Lab01_GitSetup
    git init
    git remote add origin https://github.com/lakshmi701/Lab01_GitSetup.git
2. Frontend Branch
    git checkout -b frontend
    echo "<p>Hello! My name is Lakshmi. I am a passionate learner who enjoys exploring technology, programming, and web development.</p>" > index.html
    git add index.html
    git commit -m "Added about me paragraph in index.html"
3. Main Branch
    git checkout -b main
    git merge frontend
    git push -u origin main
    git push origin frontend
4. Backend Branch
    git checkout -b backend
    echo "print('Backend API running')" > app.py
    git add app.py
    git commit -m "Added simple backend script"
    git push origin backend
5. Merge Backend to Main
    git checkout main
    git merge backend
    git push origin main
## Expected Output / Result
    Three branches: main, frontend, backend
    main branch has both index.html and app.py
    Verified using git branch and git log --oneline --graph --all
## Deliverables (what to push)
- Labs/Lab01_Setup.md (this file)
- Lab01_files/index.html and Lab01_files/app.py
## Notes / Tips
- Ignore CRLF warning on Windows.
- Use git status to check progress.
- Use git log --graph to view merges.


