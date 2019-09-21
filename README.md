# ORPHEUS

The [Orpheus Project](https://github.com/gibso/orpheus) implements a computational framework for conceptual blending with mental spaces extracted from the [ConceptNet knowledge base](https://github.com/commonsense/conceptnet5).

It was developed as artifact of my masterthesis.

### Requirements
You need [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/) and [Docker-Compose](https://docs.docker.com/compose/install/).

### Setup
Clone this repo: with its submodules:
```
 git clone --recurse-submodules git@github.com:gibso/orpheus.git
```
and enter the directory: `cd orpheus`

For running the application, execute:
```
./orpheus up
```
When running the application the first time, docker will have to pull and build images. This can take some time.
After that, you can access the application in your browser at `http://localhost`

### More Commands

You can also run the application as a daemon by running:
```
./orpheus up -d
```

Furthermore you can check out the logs by running:

```
./orpheus logs -f
```

### Develop

If you want to develop, you can use `docker-compose` commands instead of the `./orpheus` script. Then all the submodules are mounted into the services and the services run in develop mode.
Start the application in develop mode by
```
docker-compose up -d
```


### Configuration
In the file `docker-compose.prod.yml` you can specify several env variables that configure the services.
* `MAX_FACTS_PER_RELATION` specifies, how much ConceptNet facts shall be extracted for every relation
* `VALID_FACT_LANGUAGES` specifies which languages for ConceptNet nodes are allowed. The Clingo solver has some problems with foreign symbols.

## Author

Developed by Oliver Görtz.

Contact me via [GitHub](https://github.com/gibso), [XING](https://www.xing.com/profile/Oliver_Goertz9), [Facebook](https://www.facebook.com/ogoertz), [Twitter](https://twitter.com/SuperMcOli) or just write an [email](mailto:oliver.goertz@gmail.com).
