# kampagne-ai
Abhängigkeiten: Docker und Git installiert

Folgende Befehle sind in der Kommandozeile auszuführen:
```
git clone https://github.com/BravoDavo/kampagne-ai
cd kampagne-ai
docker-compose up -d
```

Der JupyterHub mit den Notebooks ist unter ```localhost:8888``` zu erreichen.

Bei Token-Abfrage mit ```docker ps``` die Docker-Container-Id ausfindig machen und mit ```jupyter notebook list``` innerhalb der Docker-Shell den Token anzeigen lassen:
```
docker ps
docker exec -it <containerId> /bin/bash
jupyter notebook list
```
Camunda ist unter ```localhost:7778``` zu erreichen.

Falls Camunda Probleme bereitet, ```docker compose build camunda1```.

Für eine Echtzeitvorhersage muss zunächst das Notebook ```Echtzeitvorhersage```, dann ```ORLDynamischerSchwellwert```` und als Letztes ```Simulation-ver_Standalone``` gestartet werden. Die anderen Notebooks lassen sich einzeln ausführen.
