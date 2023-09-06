# Project: isec6000-assignment1-task2 

## Description
repository for performing activities related to unit ISEC 6000 at Curtin University,  
Assignment 1, Task 2, 2023  

Modified Saleor stack
- Saleor Core (API) - http://localhost:8000
- Saleor Dashboard - http://localhost:9003
- React Sorefront - http://localhost:3009
- Jaeger UI (APM) - http://localhost:16686
- Mailpit - http://localhost:8025

## Requirements
1. Computer with 4 CPU and 6 GB RAM, 4 GB HD
2. OS, tested with Ubuntu 22.04
3. [Docker](https://docs.docker.com/install/)

## Instruction for deployment
1. clone the repository to the local destination
```
git clone https://github.com/Gogo72/isec6000-assignment1-task2.git
```

2. Enter the directory
```shell
cd isec6000-assignment1-task2
```

3. Build the saleor stack. (cca 15 minutes)
```shell
docker compose build
```

4. Pupolate database with initial data, create account admin@example.com:admin, (cca 5 minutes)
 ```shell
docker compose run --rm api python3 manage.py migrate
docker compose run --rm api python3 manage.py populatedb --createsuperuser
```

5. Run the application
```shell
docker compose up -d
```

## Technology used
Github, Docker, Linux, Virtual Box, Saleor-platform, React-Storefront

## Version
1.0 Initial release, 2023-09-02

## Author
Tomas Prasil

![](https://komarev.com/ghpvc/?username=Gogo72&color=yellow)
