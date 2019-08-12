pipeline {
agent any 
stages {
stage ('Compile stage') {
steps {
withMaven(maven:'-maven-3.6.1') {
sh 'mvnclean compile'
}
}
}
