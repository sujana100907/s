# s

cd C:\Users\sujan\OneDrive\Desktop\se

docker build -t calc .

docker run calc

docker ps

docker login

docker tag calc sujana1097/calc

docker push sujana1097/calc

docker ps -a

docker rm 31d8cd1020d2

docker rmi sujana1097/calc

docker ps -a

docker pull sujana1097/calc

docker run sujana1097/calc

docker ps -a


FROM node:16-alpine
WORKDIR /app
COPY calc.js /app
CMD ["node","calc.js"]


minikube start
kubectl create deployment mynginx --image=nginx
kubectl expose deployment mynginx --type=NodePort --port=90 --target-port=80
kubectl scale deployment mynginx --replicas=4
kubectl get pods
kubectl get deployments
kubectl port-forward svc/mynginx 8086:90

paste ssh key
sudo apt update
sudo apt upgrade -y
sudo apt-get install docker.io -y
sudo apt install git nano -y
git clone https://github.com/sujana100907/lasya.git
cd lasya
nano Dockerfile
sudo docker build -t suj .
sudo docker run -d -p 8098:80 suj

FROM nginx:alpine
COPY . /usr/share/nginx/html


<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>4.0.1</version>
    <scope>provided</scope>
</dependency>


# 1. Initialize a new Git repository
git init

# 2. Configure username and email
git config --global user.name "Sujana"
git config --global user.email "yourmail@gmail.com"

# 3. Check repository status
git status

# 4. Create a file
echo "Hello Git" > index.txt

# 5. Add all files to staging area
git add .

# 6. Commit the changes
git commit -m "Initial commit"

# 7. Rename current branch to main
git branch -M main

# 8. Create a feature branch
git branch feature

# 9. Switch to feature branch
git checkout feature

# 10. Make changes in the file
echo "Feature changes" >> index.txt

# 11. Stage and commit changes
git add .
git commit -m "Feature update"

# 12. Switch to main branch
git checkout main

# 13. Rebase feature branch onto main
git checkout feature
git rebase main

# 14. Switch back to main
git checkout main

# 15. Merge feature branch into main
git merge feature

# 16. Connect to GitHub repository
git remote add origin https://github.com/username/repository.git

# 17. Push changes to GitHub
git push -u origin main

# 1. Initialize repository
git init

# 2. Configure username and email
git config --global user.name "Sujana"
git config --global user.email "yourmail@gmail.com"

# 3. Create a file
echo "Hello Git" > index.txt

# 4. Add and commit the file
git add .
git commit -m "Initial commit"

# 5. Rename branch to main
git branch -M main

# 6. Display repository status
git status

# 7. Modify file
echo "New changes" >> index.txt

# 8. Display file differences
git diff

# 9. Stage and commit changes
git add .
git commit -m "Updated file"

# 10. Display all branches
git branch

# 11. Create a new branch
git branch feature

# 12. Switch to feature branch
git checkout feature

# 13. Connect to GitHub
git remote add origin https://github.com/username/repository.git

# 14. Upload changes to GitHub
git push -u origin main

# 15. Download and merge remote changes
git pull origin main

# 16. Fetch remote changes without merging
git fetch origin

# 17. Display commit history
git log --oneline

# 18. Revert the latest commit
git revert HEAD

# 19. Reset the latest commit (keeps changes staged)
git reset --soft HEAD~1

# 20. Demonstrate merge conflict

# Create feature branch
git checkout -b conflict

# Modify the file in feature branch
echo "Feature content" > index.txt

# Stage and commit
git add .
git commit -m "Feature modification"

# Switch to main branch
git checkout main

# Modify the same file in main
echo "Main content" > index.txt

# Stage and commit
git add .
git commit -m "Main modification"

# Merge feature branch into main
git merge conflict

# Resolve conflict manually by editing index.txt
# Remove conflict markers and save the file

# Stage resolved file
git add index.txt

# Complete merge
git commit -m "Resolved merge conflict"


# 1. Create a Maven Java project
mvn archetype:generate -DgroupId=com.example -DartifactId=lab-external -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

# 2. Enter the project directory
cd lab-external

# 3. Initialize Git repository
git init

# 4. Configure username and email
git config --global user.name "Sujana"
git config --global user.email "yourmail@gmail.com"

# 5. Check repository status
git status

# 6. Add project files
git add .

# 7. Commit project
git commit -m "Initial Maven project"

# 8. Rename branch to main
git branch -M main

# 9. Display commit history
git log

# 10. Display short commit history
git log --oneline

# 11. Modify a file to see differences
echo "New changes" >> README.md

# 12. Display differences
git diff

# 13. Temporarily save modifications
git stash

# 14. Display saved stash
git stash list

# 15. Restore saved modifications
git stash pop

# 16. Create a feature branch
git checkout -b feature

# 17. Make changes and commit
echo "Feature update" >> README.md
git add .
git commit -m "Feature commit"

# 18. Switch to main branch
git checkout main

# 19. Rebase feature branch onto main
git checkout feature
git rebase main

# 20. Return to main branch
git checkout main

# 21. Merge feature branch
git merge feature

# 22. Connect GitHub repository
git remote add origin https://github.com/username/repository.git

# 23. Fetch remote changes
git fetch origin

# 24. Revert latest commit
git revert HEAD

# 25. Reset latest commit (keeps changes staged)
git reset --soft HEAD~1

#scripted pipeling
stages {
    stage('Clone GitHub Repository') {
        steps {
            git branch: 'main',
                url: 'https://github.com/manisha2113/Maven-Lab.git'
        }
    }

    stage('Build Java Project') {
        steps {
            bat 'mvn clean install -f StudentApp/pom.xml'
        }
    }

    stage('Build Web Project') {
        steps {
            bat 'mvn clean package -f StudentWeb/pom.xml'
        }
    }
}
