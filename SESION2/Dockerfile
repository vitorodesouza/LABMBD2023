from amazoncorretto:21 as build

WORKDIR /app/

# Crear el archivo Main.class
#RUN javac Main.java

COPY volumen/Main.java /app/

RUN javac Main.java

FROM amazoncorretto:21 as execute

WORKDIR /app/

COPY --from=build /app/Main.class /app/Main.class

ENTRYPOINT [ "java", "Main" ]