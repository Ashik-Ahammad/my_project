## This project demonstrates essential Git practices to manage source control efficiently, including:

Initializing a Git repository.
Adding and working with feature branches.
Pushing changes to a remote repository on GitHub.
Merging pull requests and maintaining a linear commit history.

1. Set Up Git
Configuring Git username and email globally:
![Screenshot 2024-12-07 090650](https://github.com/user-attachments/assets/90770f3a-87bb-4ce1-acaf-090751b17d74)


2. Create a New Project Directory and Initialize Git
mkdir my_project  
cd my_project
git init

![Screenshot 2024-12-07 090701](https://github.com/user-attachments/assets/bc90b960-f78b-4f7c-bd99-1c82c6893ca7)


3. Add a README File and Make an Initial Commit
echo "# My Project" > README.md  
git add README.md  
git commit -m "Initial commit: Add README.md"
![Screenshot 2024-12-07 090727](https://github.com/user-attachments/assets/17eea1ad-905a-447d-a94f-6de7fb62e7bc)


4. Push the Repository to GitHub
Connect the local repository to GitHub and push the initial commit:

git remote add origin https://github.com/Ashik-Ahammad/my_project.git  
git branch -M main  
git push -u origin main  
![Screenshot 2024-12-07 090752](https://github.com/user-attachments/assets/b7579cef-0d04-4531-8047-b11f9fd6acfc)

5. Create and Work on the feature-1 Branch
Create and switch to the feature-1 branch:

git branch feature-1
git checkout feature-1  
![Screenshot 2024-12-07 090812](https://github.com/user-attachments/assets/84a7fdf6-9422-4504-884f-a999c878d942)

Add changes for feature-1 and commit:
echo "Feature 1 content" > feature1.txt  
git add feature1.txt  
git commit -m "Add feature1.txt with content for feature 1" 
![Screenshot 2024-12-07 090915](https://github.com/user-attachments/assets/a8d32b12-5e34-4c74-8dac-322350d4044b)


6. Create and Work on the feature-2 Branch
Switch back to the main branch:
git checkout main
![Screenshot 2024-12-07 090920](https://github.com/user-attachments/assets/c8852ce6-cbba-42d0-958f-d71763dc197d)


Create and switch to the feature-2 branch:
git checkout -b feature-2 
![Screenshot 2024-12-07 091018](https://github.com/user-attachments/assets/02522ab9-2fb9-46ec-bcf2-9b75b956b6ad)

Add changes for feature-2 and commit:
echo "Feature 2 content" > feature2.txt  
git add feature2.txt  
git commit -m "Add feature2.txt with content for feature 2"
![Screenshot 2024-12-07 091027](https://github.com/user-attachments/assets/e733676a-f19d-4775-b4b9-9f30b06cc75f)


7. Push Feature Branches to GitHub
Push both feature branches to the remote repository:
git push -u origin feature-1
![Screenshot 2024-12-07 091210](https://github.com/user-attachments/assets/bc5071ea-c596-413b-86be-0173ff59ac13)
git push -u origin feature-2
![Screenshot 2024-12-07 091222](https://github.com/user-attachments/assets/87f1c6da-1003-4995-b877-ed24ccb061ef)


8. Merge Branches Using Pull Requests (PRs)
Update feature-1 with the latest changes from the main branch:

git checkout feature-1  
git rebase main  
git push --force  
![Screenshot 2024-12-07 091717](https://github.com/user-attachments/assets/d8c9e7e2-9ec8-457e-b088-db038688d216)
Create a pull request (PR) for feature-1 on GitHub and merge it.

git checkout feature-2  
git rebase main  
git push --force  
![Screenshot 2024-12-07 091721](https://github.com/user-attachments/assets/3bf58373-f611-4cbd-b463-00fa137581da)
Create a pull request (PR) for feature-2 on GitHub and merge it.

9. Clean Up Local and Remote Branches
Delete the feature branches locally:
git branch -d feature-1
![Screenshot 2024-12-07 091812](https://github.com/user-attachments/assets/23b42a68-eb0e-4f21-bc3b-b3d0e7a5e41c)
git branch -d feature-2
![Screenshot 2024-12-07 091816](https://github.com/user-attachments/assets/aff98b0f-08ab-43a4-b09f-88ffad5b3b1d)

Delete the feature branches remotely:
git push origin --delete feature-1
![Screenshot 2024-12-07 091859](https://github.com/user-attachments/assets/e09e3e9d-9edc-4bc6-98e2-fa0f4d251c77)
git push origin --delete feature-2  
![Screenshot 2024-12-07 091926](https://github.com/user-attachments/assets/cddbcf2e-5257-49f2-bfab-4840ddac3d30)

10. Final Update and Submission
Updating the README.md file with all commands used, then pushing the final version:

git add README.md  
git commit -m "Update README.md with all commands used"  
git push  

