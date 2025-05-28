Program 4

package com.example;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello, Maven");
        System.out.println("This is the simple realworld example....");

        int a = 5;
        int b = 10;
        System.out.println("Sum of " + a + " and " + b + " is " + sum(a, b));
    }

    public static int sum(int x, int y) {
        return x + y;
    }
}


maven:-
mvn clean install
mvn exec:java -Dexec.mainClass="com.example.App"

gradle:-

gradle init

plugins {
    id 'java'
}

group = 'com.example'
version = '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'junit:junit:4.12'
}

task run(type: JavaExec) {
    main = 'com.example.App'
    classpath = sourceSets.main.runtimeClasspath
}

gradlew build

gradlew run




Program 7

1. sudo adduser [username]
2. When prompted, define a strong account password.
3. sudo usermod -aG sudo [username]
4. sudo su [username]
5. ssh-keygen
6. hostname -i
7. ssh-copy-id [username]@[remote-host]
8. sudo apt update
9. sudo apt install ansible -y
10. ansible --version
11. sudo mkdir -p /etc/ansible
12. sudo nano /etc/ansible/hosts
13. [local]
localhost ansible_connection=local
14. Ctrl+S, Ctrl+X
15. ansible-inventory --list -y
16. sudo ansible all -m ping




project 8: Exercise Project
Solution:
Step 1: Open GIT bash
Step 2: Create a directory with the following steps
mkdir maventest1 
cd maventest1
Step 3: Create project

mvn archetype:generate -DgroupId=com.yourname -DartifactId=repo_name-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

4. git init
5. git add .
6. git commit -m "Initial commit"
7. git branch -M main
8. git remote add origin "repo link"
9. git push -u origin main (error)
10. git pull origin main --rebase
11. git add
12. git push -u origin main
13. Go to pom.xml
