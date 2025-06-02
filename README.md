# devops-training-docker

3) 
a) docker pull nginx

b) docker images

d) docker run --name webserver -p 80:80 -v C:/Users/t3yll/Desktop/Devops/devops-training-docker/html:/usr/share/nginx/html:ro -d nginx

e) docker stop webserver 
docker rm webserver

f) docker run --name webserver -p 80:80 -d nginx 
docker cp ./html/index.html webserver:/usr/share/nginx/html/index.html

4)b)
docker build -t custom-nginx .

c)

| Aspect                       | **Volume (`-v`)**                                    | **Image personnalisée (`Dockerfile`)**                               |
| ---------------------------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **Mise à jour des fichiers** | Instantanée (modifs locales reflétées immédiatement) | Il faut re-builder l'image pour voir les changements                 |
| **Simplicité**               | Très rapide, aucun Dockerfile requis                 | Nécessite de créer un `Dockerfile` et de builder                     |
| **Portabilité**              | Moins portable (nécessite les fichiers locaux)       | Plus portable (tout est dans l'image)                                |
| **Cas d’usage**              | Parfait pour le développement                        | Parfait pour la production ou CI/CD                                  |
| **Taille de l'image**        | Aucune modification de l’image                       | L’image inclut les fichiers copiés, donc potentiellement plus lourde |
| **Sécurité**                 | Risque de fuite de fichiers locaux si mal configuré  | Contrôlé et figé dans l’image                                        |
