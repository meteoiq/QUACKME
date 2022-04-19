FROM openjdk:11

RUN apt-get clean
RUN apt-get update 
RUN apt-get install -y maven

# build
WORKDIR /root
COPY . /root
RUN rm -Rf /root/target/*
RUN mvn -DskipTests=true clean install

# run
WORKDIR /root
ENTRYPOINT ["java","-Xmx3500m", "-jar","target/mars-obspro-quackmeweb-backend-0.0.1-SNAPSHOT.jar"]
