FROM nginx:1.21

COPY ./conf/default.conf /etc/nginx/conf.d/default.conf

COPY ./html/index.html /usr/share/nginx/html/index.html

RUN echo "mynginx image built successfully."

ENV TEST_VALUE1="test_value1"

ENV TEST_VALUE2="test_value2"

EXPOSE 8000