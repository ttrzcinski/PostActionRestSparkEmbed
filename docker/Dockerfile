FROM openjdk:8u342-jre-slim-bullseye
# Used to be java:8

RUN apt-get update
RUN apt-get install -y maven

ADD . /code
WORKDIR /code

RUN ["mvn", "clean", "install"]

EXPOSE 4567

CMD ["java", "-jar", "target/parse-jar-with-dependencies.jar"]