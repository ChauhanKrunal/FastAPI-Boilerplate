# install python in the container
FROM python:3.8.8-slim 
# copy the local requirements.txt file to the 
# /app/requirements.txt in the container
# (the /app dir will be created)
COPY ./requirements.txt /app/requirements.txt
# install the packages from the requirements.txt file in the container
RUN pip install -r /app/requirements.txt
# expose the port that uvicorn will run the app
# copy the local app/ folder to the /app fodler in the container
COPY . /app
# set the working directory in the container to be the /app
WORKDIR /app
# expose the port
EXPOSE 8000
# execute the command python main.py (in the WORKDIR) to start the app
CMD [ "python3","main.py" ]