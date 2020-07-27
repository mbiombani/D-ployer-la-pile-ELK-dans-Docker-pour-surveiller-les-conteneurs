# Project Title

Déployer la pile ELK dans Docker pour surveiller les conteneurs

## Getting Started

Nous utiliserons docker-compose pour déployer notre pile ELK. Docker-compose nous offre une solution pour déployer plusieurs conteneurs en même temps.

### Prerequisites

```
Docker
Docker-Compose
```

### Installing

Démarrez les conteneurs à l'aide de Docker-compose.

```
git clone https://github.com/mbiombani/D-ployer-la-pile-ELK-dans-Docker-pour-surveiller-les-conteneurs.git
cd D-ployer-la-pile-ELK-dans-Docker-pour-surveiller-les-conteneurs
docker-compose up -d
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Si vous configurez plusieurs pipelines, il peut être utile de déboguer votre conteneur Logstash. Vous pouvez utiliser docker execpour déboguer votre conteneur Logstash et vérifier les fichiers de configuration. Ceci est hors de portée de notre configuration de base actuelle.

```
docker exec -it docker-elk_logstash_1 bash
cat /usr/share/logstash/pipeline/logstash.conf 
```


## Deployment

Nous allons démarrer un conteneur Nginx supplémentaire à l'aide de la CLI Docker.

```
docker run -d -p 8080: 80 --log-driver gelf --log-opt gelf-address = udp: // localhost: 12201 nginx: dernier
```
