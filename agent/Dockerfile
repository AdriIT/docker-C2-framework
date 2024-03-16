FROM python:3.9

USER root

RUN apt update
RUN apt-get install iputils-ping -y
#RUN apt install -y python-pip
RUN mkdir /.agent 
# Copy the directory inside /agent on the container
COPY . /.agent
RUN rm /.agent/Dockerfile
# Set workdir on container
WORKDIR /

# Install Agent dependancies on the container
RUN pip install pynput

RUN pip install websocket-client
RUN pip install psutil
# Start script
#CMD [""]
CMD ["python", ".agent/agent.py"]

