# docker-essentials

## Run code
To run the Flask app, do the following:

1. Start the docker (if not).
```bash
systemctl start docker
```
2. Build the docker image.
```bash
cd hello-world
docker image build -t python-hello-world .
```
3. Verify if the image is build.
```bash
docker image ls
```
4. Run the build image
```bash
docker run -p 5001:5000 -d python-hello-world
```
5. Navigate the link `http://localhost:5001`
6. Check the log output by
```bash
docker container logs [container_id]
```
`[container_id]` can be obtained by running the command
```bash
docker container ls
```
7. Remove the containers
```bash
docker container stop [container_id]
docker system prune
```
