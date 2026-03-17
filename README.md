# Frontend

The frontend is the service in RobotShop to serve the web content over nginx pod on eks cluster using alb .


Let's download the HTDOCS content and deploy under the Nginx path.

```
# curl -s -L -o /tmp/frontend.zip "https://github.com/roboshop-devops-project/frontend/archive/main.zip"
```

Deploy in Nginx Default Location.

```
# cd /usr/share/nginx/html
# rm -rf * 
# unzip /tmp/frontend.zip
# mv frontend-main/* .
# mv static/* .
# rm -rf frontend-master README.md
# mv localhost.conf /etc/nginx/default.d/roboshop.conf
```

Build docker image as mention in this repo and deploy using jenkins on eks cluster.  

Make changes accordingly alb and ecr repo.

```

```
