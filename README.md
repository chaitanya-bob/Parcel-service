sudo apt update
sudo apt install -y openjdk-11-jdk
Verify the installation:

bash
java -version
Install Maven: If Maven is not already installed, use:

bash
sudo apt install -y maven
Verify the installation:

bash
mvn -version
Set Environment Variables: Ensure JAVA_HOME is set to the Java 11 installation path. Add the following lines to your .bashrc or .zshrc file:

bash
export JAVA_HOME=$(dirname $(dirname $(readlink -f $(which java))))
export PATH=$JAVA_HOME/bin:$PATH
Apply the changes:

bash
source ~/.bashrc
Build the Project
To build the project, use the following commands:

Navigate to the Project Directory:

bash
cd /path/to/simple-parcel-service-app
Clean and Build the Project:

bash
mvn clean install
This command will:
Download dependencies
Compile the source code
Run tests
Package the application into a JAR file (target/simple-parcel-service-app-1.0-SNAPSHOT.jar)
Run the Application
You can run the application in two ways:

1. Using Maven:
bash

mvn spring-boot:run

3. Using the Packaged JAR:
After building the project, run the packaged JAR file:

bash

java -jar target/simple-parcel-service-app-1.0-SNAPSHOT.jar
The application will start and be accessible at http://localhost:8080

