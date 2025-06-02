# devops-training-docker

3) 
a) docker pull nginx

b) docker images

d) docker run --name webserver -p 80:80 -v C:/Users/t3yll/Desktop/Devops/devops-training-docker/html:/usr/share/nginx/html:ro -d nginx

e) docker stop webserver 
docker rm webserver

f) docker run --name webserver -p 80:80 -d nginx 
docker cp ./html/index.html webserver:/usr/share/nginx/html/index.html