mkdir Git_Project
cd Git_Project
git init
touch app.py
print("Hello, Git & GitHub!")
git status
git add app.py
git commit -m "Initial commit: add app.py with basic Python code"
git remote add origin <your-repository-url>
git remote -v
git push -u origin master
