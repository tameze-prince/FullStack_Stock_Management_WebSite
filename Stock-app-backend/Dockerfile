FROM eclipse-temurin:21-jre-alpine

WORKDIR /app

# Copy the fat JAR
COPY target/*.jar app.jar

# Expose port
EXPOSE 8080

# Health check
HEALTHCHECK --interval=30s --timeout=3s --start-period=60s \
  CMD wget --no-verbose --tries=1 --spider http://localhost:8080/actuator/health || exit 1

# JVM optimizations for 512MB RAM
ENV JAVA_OPTS="-Xms128m -Xmx400m -XX:+UseSerialGC -XX:MaxMetaspaceSize=128m -XX:CompressedClassSpaceSize=32m -Xss256k -XX:+TieredCompilation -XX:TieredStopAtLevel=1 -Djava.security.egd=file:/dev/./urandom"

# Run application
CMD ["sh", "-c", "java $JAVA_OPTS -jar app.jar"]