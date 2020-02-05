# Systems for Big Data Analytics - Labs

This is a setup for the course Big Data Analysis @ Telecom (Master 2 Data Science Polytechnique).

## Hadoop cluster

Needs `docker` and `docker-compose`:

- https://www.docker.com/
- https://docs.docker.com/compose/

Run the Hadoop cluster on your machine:

```
docker-compose up
```

Stop it with `Ctrl+C`.

## TP1 : MapReduce

### Setup

Needs `nix`:

- https://nixos.org/nix/

Open a Nix shell with:

```
nix-shell
```

It will give you a Java environment, `gradle` and `hadoop`:

- https://gradle.org/
- https://hadoop.apache.org/

### Build the JAR

```
gradle TP1:jar
```

### Download data

```
curl -L https://www.dropbox.com/s/o7a9e8cdu7gm7ms/lorem.txt -o data/input/lorem.txt
```

### Run

```
hadoop jar TP1/build/libs/TP1.jar data/input data/output
```
