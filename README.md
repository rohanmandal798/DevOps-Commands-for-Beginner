# DevOps-Commands-for-Beginner

# 1. Git Commands

| Command                                      | Description                   |
| -------------------------------------------- | ----------------------------- |
| `git --version`                              | Check Git version             |
| `git config --global user.name "yourname"`   | Set global username           |
| `git config --global user.email "youremail"` | Set global email              |
| `git init`                                   | Initialize Git repository     |
| `git clone <repo_url>`                       | Clone a repository            |
| `git status`                                 | Check repository status       |
| `git add <file>`                             | Add specific file             |
| `git add .`                                  | Add all files                 |
| `git commit -m "message"`                    | Commit changes                |
| `git push origin <branch>`                   | Push to remote repository     |
| `git pull origin <branch>`                   | Pull latest changes           |
| `git branch`                                 | List branches                 |
| `git checkout <branch>`                      | Switch branch                 |
| `git checkout -b <new_branch>`               | Create & switch to new branch |
| `git merge <branch>`                         | Merge branch                  |
| `git log --oneline --graph --all`            | Show commit history           |

---

# 2. Docker Commands

| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `docker --version`                         | Check Docker version           |
| `docker ps`                                | List running containers        |
| `docker ps -a`                             | List all containers            |
| `docker images`                            | List images                    |
| `docker pull <image_name>`                 | Pull an image                  |
| `docker run -d -p 8080:80 <image_name>`    | Run container in detached mode |
| `docker run -it <image_name> /bin/bash`    | Run interactive container      |
| `docker stop <container_id>`               | Stop container                 |
| `docker start <container_id>`              | Start container                |
| `docker rm <container_id>`                 | Remove container               |
| `docker rmi <image_id>`                    | Remove image                   |
| `docker build -t <image_name> .`           | Build image from Dockerfile    |
| `docker logs <container_id>`               | View container logs            |
| `docker exec -it <container_id> /bin/bash` | Access container shell         |

---

# 3. Kubernetes (kubectl) Commands

| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `kubectl version --client`                 | Check kubectl version          |
| `kubectl cluster-info`                     | Cluster information            |
| `kubectl get nodes`                        | List nodes                     |
| `kubectl get pods -A`                      | List pods in all namespaces    |
| `kubectl get pods`                         | List pods in current namespace |
| `kubectl get svc`                          | List services                  |
| `kubectl get deployments`                  | List deployments               |
| `kubectl describe pod <pod_name>`          | Describe pod details           |
| `kubectl logs <pod_name>`                  | View pod logs                  |
| `kubectl exec -it <pod_name> -- /bin/bash` | Access pod shell               |
| `kubectl apply -f <file.yaml>`             | Apply configuration            |
| `kubectl delete -f <file.yaml>`            | Delete resources               |
| `kubectl delete pod <pod_name>`            | Delete pod                     |
| `kubectl rollout status deployment/<name>` | Check rollout status           |
| `kubectl get all`                          | List all resources             |

---

# 4. AWS CLI Commands

| Command                                       | Description           |
| --------------------------------------------- | --------------------- |
| `aws --version`                               | Check AWS CLI version |
| `aws configure`                               | Configure AWS CLI     |
| `aws sts get-caller-identity`                 | Show current identity |
| `aws s3 ls`                                   | List S3 buckets       |
| `aws s3 ls s3://<bucket_name>`                | List files in bucket  |
| `aws s3 cp <file> s3://<bucket_name>/`        | Upload file to S3     |
| `aws ec2 describe-instances`                  | List EC2 instances    |
| `aws ec2 start-instances --instance-ids <id>` | Start EC2 instance    |
| `aws ec2 stop-instances --instance-ids <id>`  | Stop EC2 instance     |
| `aws iam list-users`                          | List IAM users        |
| `aws iam list-roles`                          | List IAM roles        |
| `aws eks list-clusters`                       | List EKS clusters     |
| `aws eks update-kubeconfig --name <cluster>`  | Update kubeconfig     |

---

# 5. Linux / Unix Commands

| Command                   | Description              |
| ------------------------- | ------------------------ |
| `pwd`                     | Print working directory  |
| `ls -l`                   | List files (long format) |
| `cd <dir>`                | Change directory         |
| `cd ..`                   | Go to parent directory   |
| `mkdir <dir>`             | Create directory         |
| `rm <file>`               | Remove file              |
| `rm -rf <dir>`            | Remove directory         |
| `cp <src> <dest>`         | Copy file/directory      |
| `mv <src> <dest>`         | Move/Rename file         |
| `cat <file>`              | Display file content     |
| `less <file>`             | View file page by page   |
| `grep "text" <file>`      | Search text in file      |
| `find . -name filename`   | Search file by name      |
| `ps`                      | List running processes   |
| `top`                     | Monitor system processes |
| `df -h`                   | Disk space usage         |
| `du -sh <dir>`            | Folder size              |
| `chmod 755 <file>`        | Change permissions       |
| `chown user:group <file>` | Change ownership         |

---

# 6. Jenkins Commands

| Command                                | Description           |
| -------------------------------------- | --------------------- |
| `java --version`                       | Check Java version    |
| `jenkins --version`                    | Check Jenkins version |
| `systemctl status jenkins`             | Jenkins status        |
| `systemctl start jenkins`              | Start Jenkins         |
| `systemctl stop jenkins`               | Stop Jenkins          |
| `systemctl restart jenkins`            | Restart Jenkins       |
| `tail -f /var/log/jenkins/jenkins.log` | View Jenkins logs     |

---

# 7. Terraform Commands

| Command               | Description             |
| --------------------- | ----------------------- |
| `terraform --version` | Check Terraform version |
| `terraform init`      | Initialize Terraform    |
| `terraform plan`      | Show execution plan     |
| `terraform apply`     | Apply changes           |
| `terraform destroy`   | Destroy infrastructure  |
| `terraform fmt`       | Format configuration    |
| `terraform validate`  | Validate configuration  |

---

# 8. Ansible Commands

| Command                            | Description           |
| ---------------------------------- | --------------------- |
| `ansible --version`                | Check Ansible version |
| `ansible all -m ping`              | Ping all hosts        |
| `ansible all -m setup`             | Gather system facts   |
| `ansible-playbook <playbook.yaml>` | Run playbook          |
| `ansible-vault encrypt <file>`     | Encrypt file          |
| `ansible-vault decrypt <file>`     | Decrypt file          |
| `ansible-galaxy list`              | List installed roles  |

---

# 9. Useful One-Liners

### Stop all running Docker containers

```bash
docker ps -aq | xargs docker stop
```

### Remove all Docker containers

```bash
docker ps -aq | xargs docker rm
```

### Remove all Docker images

```bash
docker images -q | xargs docker rmi -f
```

### List all Kubernetes pods with details

```bash
kubectl get pods -A -o wide
```

### List all Kubernetes nodes with details

```bash
kubectl get nodes -o wide
```

### Show pod resource usage

```bash
kubectl top pods -A
```

### Show node resource usage

```bash
kubectl top nodes
```

### Show disk usage

```bash
df -h | grep -v tmpfs
```

### Show largest folders

```bash
du -h --max-depth=1 | sort -hr
```



This progression follows the typical DevOps learning path and makes each subsequent tool easier to understand.
