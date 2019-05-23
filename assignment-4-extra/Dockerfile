FROM httpd:2.4

RUN apt-get update \
    && apt-get install -y mc \
    && apt autoremove \
    && rm -rf /var/lib/apt/lists/
