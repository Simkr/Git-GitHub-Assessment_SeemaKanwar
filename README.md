Question 1: Project Initialization & First Push
==============================================
Create a new folder for your project
mkdir Git_GitHub_Assessment
cd Git_GitHub_Assessment

Initialize a Git repository
git init

Create a file named app.py and add some Python code
vi app.py
print("Hello, Git & GitHub!")

Check the current Git status
git status

Stage the file
git add app.py

Commit with a meaningful message
git commit -m "Initial commit: add app.py with basic Python code"

Create a remote repository (GitHub or similar)
https://github.com/Simkr/Git-GitHub-Assessment_SeemaKanwar.git

Add the remote (origin) to your local repo
git remote add origin https://github.com/Simkr/Git-GitHub-Assessment_SeemaKanwar.git

Verify the remote configuration
git remote -v

Push your code to the remote repository
git push -u origin master

<img width="891" height="677" alt="image" src="https://github.com/user-attachments/assets/ce55a1a9-cfbc-4365-8343-4ec75c6afb46" />
<img width="851" height="550" alt="image" src="https://github.com/user-attachments/assets/1f8061ab-5f21-4ccd-8b43-ac5d9417e101" />

Question 2: Working with Changes & History
============================================
1. Modify app.py by adding new functionality
vi app.py

2. Check what changes are made before staging
git status

3. View differences in the file
git diff

4. Stage only specific changes (partial staging)
git add -p app.py

5. Commit with a clear message
git commit -m "Add greet function to app.py"

6. Make another change in app.py
vi app.py

7. Stage all changes
git add app.py

(or everything:)
git add .

8. Commit again
git commit -m "Add farewell function"

9. View full commit history
git log

10. View compact (one-line) history
git log --oneline

<img width="887" height="654" alt="image" src="https://github.com/user-attachments/assets/e6e89a2f-242a-49b7-aeb5-344f36d954bd" />
<img width="869" height="470" alt="image" src="https://github.com/user-attachments/assets/54790d2e-17f1-47e9-97e9-37352ea3c61e" />
<img width="708" height="691" alt="image" src="https://github.com/user-attachments/assets/06cac2e7-ebdc-4a78-8d64-9116a0dfaf0a" />

Question 3: Branching & Feature Development
============================================

Create a new branch (e.g., feature-update)
git branch feature-update

Switch to the new branch
git switch feature-update

Modify app.py with new feature logic
vi app.py
def greet(name):
    return f"Hello, {name}!"

def new_feature():
    return "This is a new feature!"

print(greet("Seema"))
print(new_feature())

Stage and commit the changes
git add app.py
git commit -m "Add new_feature function in feature-update branch"

Switch back to the main branch
git switch master

Merge the feature branch into main
git merge feature-update

Verify changes are merged
cat app.py
def greet(name):
    return f"Hello, {name}!"
def new_feature():
    return "This is a new feature!"
print(greet("Seema"))
print(new_feature())

Delete the branch safely
git branch -d feature-update

Try force deleting a branch (create a dummy branch for this)
git switch -c temp-branch
echo "# temp change" >> app.py
git add app.py
git commit -m "Temp commit"
git switch master
git branch -D temp-branch
<img width="803" height="344" alt="image" src="https://github.com/user-attachments/assets/2625b01d-ca5d-43a0-a63b-36f7df2b4f89" />
<img width="811" height="633" alt="image" src="https://github.com/user-attachments/assets/ac0b3237-554e-4cc1-9f30-1155a33866a9" />
<img width="804" height="377" alt="image" src="https://github.com/user-attachments/assets/c45658db-0192-4c00-9ae6-f65156161e9a" />




