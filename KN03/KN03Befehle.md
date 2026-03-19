```sh
docker network create --driver bridge --subnet 172.18.0.0/16 tbz
```
Erstellt ein eigenes Docker-Netzwerk

Um Kontrolle über IPs und Kommunikation zu haben

- `docker network create` neues Netzwerk erstellen  
- `--driver bridge` normales Bridge-Netzwerk (wie default, aber selbst erstellt)  
- `--subnet 172.18.0.0/16` eigener IP-Bereich  
- `tbz` Name des Netzwerks  


```sh
docker network ls
```
Zeigt alle Netzwerke 

Um zu prüfen, ob ein Netzwerk existiert
- `bridge` = Standart
- `host`= direkt Host
- `none`= kein Netzwerk
- `tbz` = neues Netzwerk

```sh
docker inspect tbz
```

Zeigt alle Infos über mein Netzwerk
Zum Analysieren

- Subnet (172.18.0.0/16)  
- Gateway (z.B. 172.18.0.1)  
- verbundene Container  

```bash
docker inspect bridge
```

Infos über das default bridge Netzwerk

Unterschied:
- weniger Kontrolle
- keine eigene Konfiguration

```bash
docker run -dit --name busybox1 busybox sh
```

Startet Container im default bridge

- `-d`  im Hintergrund  
- `-i`  interaktiv  
- `-t`  Terminal  
- `--name busybox1`  Name  
- `busybox1`  Image  
- `sh`  Shell starten  

```bash
docker run -dit --name busybox3 --network tbz busybox sh
```
Startet Container im tbz Netzwerk

- `--network tbz`  wichtig  

```bash
docker exec -it busybox3 sh
```
Öffnet Terminal im Container

Du arbeitest jetzt im Container selbst

```bash
ifconfig
```
Zeigt Netzwerkdaten im Container

- IP-Adresse  
- Interface (eth0)  
- etc.  