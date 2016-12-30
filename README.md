# Docker-Nexus-IQ
Docker container that runs Nexus IQ

This Docker image builds a CentoOS machine, installs some bits including Oracle jdk. It then downloads and runs Nexus IQ Server within the container.  

Build command - ensure the Docker file is in the same directory. Notice the trailing dot :)
docker build -t <YOUR NAME>/nexus-iq:v1-24 .

Run command. This will bind the internal container port to 8072 on your host machine
docker run -d -p 8072:8070 --name nexus-iq <YOUR NAME>/nexus-iq:v1-24

Navigate to http://localhost:8072 assuming Docker in running locally
