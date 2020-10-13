# this branch is meant for lab4&5
this repo is a clone of https://github.com/miguelgrinberg/flasky
![stamp](https://github.com/isamumu/ECE444-F2020-Lab3/blob/docker/docker1000.PNG)
![stamp](https://github.com/isamumu/ECE444-F2020-Lab3/blob/docker/docker1.PNG)
![stamp](https://github.com/isamumu/ECE444-F2020-Lab3/blob/docker/docker3.PNG)
![stamp](https://github.com/isamumu/ECE444-F2020-Lab3/blob/docker/docker2.PNG)


<br>
2) in order to build and start the system, one must first locate their files in one folder, and enter its directory using command line. Then, one must install docker from the following website: https://www.docker.com/. Following installation, one must create a plain Dockerfile which contains information specified as follows: 

                              FROM python:3.7	
                              COPY . /app	
                              WORKDIR /app	
                              RUN pip install -r requirements.txt	
                              ENTRYPOINT ["python3"]	
                              CMD ["hello.py"]

Additionally, the main python file should be modified in order for it to run on localhost: 
![stamp](https://github.com/isamumu/ECE444-F2020-Lab3/blob/docker/localhost.PNG)

Next, on the command line, the two commands must be run in sequence: 
1. docker build -t flask-sample:latest .
2. docker run -d -p 5000:5000 flask-sample

One can now test the webpage by entering the URL, on a browser which the docker terminal outputs

3) Docker is a container based, which are just user spaces in an operating system. Docker containers share the OS container. A Virtual Machine is not a container technology, and instead are made up of user space and kernel space of an operating system. Essentially, Docker containers are less expensive memory wise than Virtual Machines because they do not qrequire a operating system to be installed. VMs in general involve more overhead beyong what is being consumed by the application being run. 
