FROM nginx:latest  
#  Welches Image Docker benutzen sollte
WORKDIR /usr/share/nginx/html
# "cd /usr/share/nginx/html" im Container
COPY helloworld.html . 
# Kopiert lokaler Pfad im Projektverzeichnis in Pfad wo es im Docker Container landen soll
EXPOSE 	80	
# Port 80 frei geben
