## CVAT


### Prerequisites
1. [Docker](https://docs.docker.com/engine/install/)
2. [Docker Compose](https://docs.docker.com/compose/install/)
3. [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### Installation
#### Step 1: Clone Repository
```commandline
git clone https://github.com/opencv/cvat.git
cd cvat
```
#### Step 2: Run Docker
Note: Make sure ```docker```/```docker desktop``` is running.
On the command line:
```commandline
docker compose up -d
```
#### Step 3: Creating Superuser
Enter docker container:
```commandline
docker exec -it cvat_server /bin/bash
```
Run following on containers commandline:
:
```commandline
python3 ~/manage.py createsuperuser
```

Provide ```Username``` and ```Password``` to superuser, email can be left blank.

Access ```localhost:8080``` to open the CVAT UI (Chrome is recommended). Use superuser credentials
to log in. After logging in [create a ```Project```](https://opencv.github.io/cvat/docs/manual/advanced/projects/).
Open the ```Project``` and [create a ```Task```](https://opencv.github.io/cvat/docs/manual/basics/creating_an_annotation_task/)

Note: To restart CVAT run ```docker compose up -d```

For more info: https://opencv.github.io/cvat/docs/administration/basics/installation/#windows-10
