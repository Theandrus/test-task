FROM python:3.8
ENV PYTHONUNBUFFERED 1
RUN mkdir /ai_clinic_task
WORKDIR /ai_clinic_task
ADD . /ai_clinic_task/
RUN pip install --upgrade pip && pip install -r requirements.txt
RUN pip install mysqlclient
COPY . /ai_clinic_task/