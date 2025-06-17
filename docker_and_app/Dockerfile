FROM public.ecr.aws/docker/library/python:3.11-slim

WORKDIR /usr/src/app

COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt

COPY streamlit_app.py streamlit_app.py

COPY aws_logo.png aws_logo.png

EXPOSE 80

ENTRYPOINT [ "streamlit", "run", "app.py", \
    "--server.enableCORS", "true", \
             "--server.port", "80", \
             "--browser.serverPort", "80"]
