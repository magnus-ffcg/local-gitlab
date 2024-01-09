# Gitlab

## Register gitlab.local in /etc/hosts or likeworthy

 ```
 ::1  gitlab.local
 ```

## Start gitlab

GITLAB_HOME=$(pwd) docker compose up -d

## Get "root" password

docker exec -it $(docker ps | grep "gitlab-ce" | awk '{print $1}') grep 'Password:' /etc/gitlab/initial_root_password | awk '{print $2}'

## Login with root

Visit: http://127.0.0.1

* Username: root
* Password: (above password)