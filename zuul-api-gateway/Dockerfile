# Stage 1: Build stage
FROM maven:3.8.4-openjdk-11 AS build

# Set the working directory to /app
WORKDIR /app

# Copy the entire project to the container
COPY . .

# Build the application using Maven
RUN mvn clean package -DskipTests

# Stage 2: Production stage
FROM openjdk:11.0.10-jre

# Set the working directory to /app
WORKDIR /app

# Copy the jar file from the build stage to the production stage
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app/zuul.jar

# Expose port 9999
EXPOSE 9999

# Start the application using the jar file
CMD ["java", "-jar", "zuul.jar"]



# FROM maven as build 
# WORKDIR /app
# COPY . .
# RUN mvn install 

# FROM openjdk:11.0.10-jre
# WORKDIR /app
# COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app
# EXPOSE 9999
# CMD ["java","-jar","zuul-0.0.1-SNAPSHOT.jar"]