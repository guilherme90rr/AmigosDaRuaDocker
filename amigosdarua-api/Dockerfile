# Use uma imagem do Maven como base
FROM maven:3.8.4-openjdk-11

# Defina o diretório de trabalho
WORKDIR /app

# Copie o arquivo pom.xml para o contêiner
COPY pom.xml .

# Baixe as dependências do Maven
RUN mvn dependency:go-offline

# Copie o código-fonte do seu projeto para o contêiner
COPY src ./src

# Compile o projeto
RUN mvn package

# Execute o aplicativo Java
CMD ["java", "-jar", "target/AmigosDaRua.jar"]