FROM maven:3.5
EXPOSE 8080
WORKDIR /opt/shipping-app
COPY src/ .
COPY *.xml .
RUN mvn clean package
RUN mv target/shipping-1.0.jar shipping.jar
ENV CART_ENDPOINT="cart:8080"
    DB_HOST="mysql"