FROM maven:3.9.11
EXPOSE 8080
WORKDIR /opt/shipping-app
COPY pom.xml .
COPY src ./src
RUN mvn clean package
RUN mv target/shipping-1.0.jar shipping-1.0.jar
ENV CART_ENDPOINT="cart:8080" \
    DB_HOST="mysql"
CMD ["java", "-jar", "shipping.jar"]