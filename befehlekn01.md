`docker version`: Version anzeigen  
`docker search {image}`: image im docker registry suchen  
`docker pull {image}`: image mit dem name "image" lokal herunterladen  
`docker create {image}`: Container mit dem image "image" erstellen  
`docker start {container}`: Container mit dem namen "container" starten  
`docker run {image}`: docker pull {image}; docker create {image}; docker start {container mit {image}}  
`docker exec {container} {linux/shell command}`: im laufenden {container} {linux/shell command} ausführen  
`docker ps`: laufende Docker conainer auflisten (nichtlaufende mit -a anzeigen)  
`docker stop {container}`: {container} ausschalten  
`docker rm {container...}`: {container...} löschen  
`docker rmi {image...}`: lokales {image...} löschen
