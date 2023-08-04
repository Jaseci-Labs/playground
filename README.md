# Jaseci Playground

## How to run

1. Install [Docker](https://docs.docker.com/get-docker/)
2. Pull the [jaseci/jaseci](https://hub.docker.com/r/jaseci/jaseci) image with

```bash
docker pull jaseci/jaseci
```

3. install pm2 with

```bash
npm install pm2 -g
```

4. then run

```bash
pm2 start --name 'jaseci-playground' index.js
```

5. go to `localhost:3000` in your browser
6. To stop the server run

```bash
pm2 stop jaseci-playground
```

## How to create new examples and add them to the playground

1. Create the JAC file you need in the `public/examples` folder
2. cd into the `public/examples` folder
3. run

```bash
python create.py
```

## Features

- Multiple JAC Examples
- Support Multiple Versions of Jaseci

## Todo

- [ ] Add more examples
- [ ] Working Docker Implementation (As for each execution of the Jaseci Playground, a new docker container is created, the docker in docker approach is taken but was unable to find a way to use the inside docker socket)
- [ ] Cannot build dependant JAC files (e.g. if a JAC file depends on another JAC file, the playground will not be able to run it)
- [ ] Dedicated Terminal for the User to interact with the Jaseci Instance
