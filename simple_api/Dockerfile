FROM python:latest
MAINTAINER abdoulrahimbarry
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip3 install flask flask_httpauth flask_simpleldap python-dotenv
#COPY ./student_age.py /
COPY $GITHUB_WORKSPACE/simple_api/student_age.py /
VOLUME ["/data"]
COPY $GITHUB_WORKSPACE/simple_api/student_age.json /data/student_age.json
RUN ls /data
EXPOSE 5000
CMD ["python", "./student_age.py"]