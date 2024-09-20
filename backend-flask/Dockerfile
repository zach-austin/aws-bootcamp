FROM python:3.10-slim-buster

# Inside container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# Copies file containing libraries we want to install 
COPY requirements.txt requirements.txt

# Inside Container
# Installs python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means current directory
COPY . .

# Sets Environment Variable (Env Vars) inside container
ENV FLASK_ENV=development


EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]