


C:\Learning\CoreAPI>

$ docker --version
$ docker build -t mydockerapp .
$ docker images


// to run docker
				   ip:port		instance_name	
$docker run -d -p 15001:80 --name dc1 mydockerapp

//http://localhost:15001/api/values

$docker run -d -p 15002:80 --name dc1  --env ASPNETCORE_ENVIORNMENT=QA mydockerapp
$docker run -d -p 15003:80 --name dc1  --env ASPNETCORE_ENVIORNMENT=Staging mydockerapp
$docker run -d -p 15004:80 --name dc1  --env ASPNETCORE_ENVIORNMENT=Production mydockerapp


// show all containers running
$ docker ps

// show all containers
$ docker ps -a

			[containerID]
$docker stop c57f647b987b 

$docker start c57f647b987b 

// remove container
$docker rm c57f647b987b 

// remove images
			[imageID]
$docker rmi c57f647b987b 

// Image with version  [image version]
docker tag mydockerapp mydockerapp:v1
									  [image version]
$docker run -d -p 15001:80 --name dc1 mydockerapp:v1

// change some thing - now both have different images
docker run -d -p 15002:80 --name dc2 mydockerapp



// push to Docker HUB
docker tag mydockerapp ashishsinghusa/mydockerapp:v1.0
docker push ashishsinghusa/mydockerapp:v1.0

docker pull ashishsinghusa/mydockerapp:v1.0


docker run -d -p 15009:80 --name repo1 ashishsinghusa/mydockerapp:v1.0