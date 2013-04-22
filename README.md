szjug_workshop_2013
===================

1. Jenkins overview

http://jenkins-ci.org/  
https://issues.jenkins-ci.or  
https://wiki.jenkins-ci.org/display/JENKINS/Beginners+Guide+to+Contributing  

2. Konto na github
3. sklonować https://github.com/jenkinsci/jenkins
4. sklonować repo do workspace

        mkdir jenkins
        cd jenkins
        git clone https://github.com/kardigen/jenkins.git
        git status

5. utworzyć working branche

        git branch JENKINS-12471
        git status
        git checkout JENKINS-12471
        git status
        
6. uruchomić testy

        mvn clean test
        
        mvn clean install -pl war -am -DskipTests
        mvn clean test
        
        export MAVEN_OPTS="-Xmx512m -XX:MaxPermSize=128m"
        mvn clean install -pl war -am -DskipTests
        mvn test
        
7. poprawić problem
