szjug_workshop_2013
===================

# Jenkins overview

http://jenkins-ci.org/  
https://issues.jenkins-ci.or  
https://wiki.jenkins-ci.org/display/JENKINS/Beginners+Guide+to+Contributing  

# github

1. Konto na github
2. sklonować https://github.com/jenkinsci/jenkins
3. sklonować repo do workspace

        mkdir jenkins
        cd jenkins
        git clone https://github.com/kardigen/jenkins.git
        git status

# utworzyć working branche

        git branch JENKINS-12471
        git status
        git checkout JENKINS-12471
        git status
        
# uruchomić testy

        mvn clean test
        
        mvn clean install -pl war -am -DskipTests
        mvn clean test
        
        export MAVEN_OPTS="-Xmx512m -XX:MaxPermSize=128m"
        mvn clean install -pl war -am -DskipTests
        mvn test
        
# zaimportować projekt do IDE

  Po uruchmieniu IntelliJ Idea użyć opcji:
  - Importuj projekt
  - wskazać katalog z git workspace
  - import from external model->maven
  - search project recursively
  - import maven projects automatically
  - next,next
  - choose java jdk dir
  - finish

# podstawowe skróty

  - uruchamiane akcji - ctrl/cmd + shift + a
  - find in paths - ctrl + shift + f
  - opcje szukaj: całe słowa, maska pliku: *.properties
  - zamieniamy messages

# komitowanie i wypychanie zmian

        git add
        git commit -m 'message'
        git rebase master
        git checkout master
        git rebase JENKINS-12471
        git push

