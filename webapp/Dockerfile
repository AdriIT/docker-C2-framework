FROM python:3.9
ENV PYTHONUNBUFFERED 1

#RUN apt install python3.11-venv

RUN mkdir server
COPY . ./server

#COPY src /src/
#COPY packaging/entrypoint.sh entrypoint.sh
#
#RUN chmod +x entrypoint.sh


#RUN python3 -m venv venv
#RUN source venv/bin/activate
RUN python -m pip install -U 'channels[daphne]'
RUN python3 -m pip install channels_redis

#ENV DJANGO_SETTINGS_MODULE=config.settings

EXPOSE 8000

WORKDIR ./server
#ENTRYPOINT ["/entrypoint.sh"]
ENTRYPOINT ["python", "manage.py"]
CMD ["runserver", "0.0.0.0:8000"]


