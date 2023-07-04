FROM python:3.10-slim-buster

# makes a directory inside the Container 
WORKDIR /backend-flask

# copies the file req from actual machine to the container that we are creating
COPY requirements.txt requirements.txt

# install the libraries inside the container with the -r switch which lists the libararies
RUN pip3 install -r requirements.txt

# . means everything in the current directory - linux things 
# the first period represents everything inside the backend-flask directory 
# the second period represents everything /backend-flask inside the container 
# line 4 represents the current directory and . means the current directory so essentially we are copying everything from outside current dir to containers current dir
COPY . .

# ENV ways to configure our applications 
# Inside the containers and will remain set when the container is running 
ENV FLASK_ENV=development


EXPOSE ${PORT}

# cmd stands for command 
# 
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]