pipeline {
agent any
stages {
stage("Creating Inventory") {
steps {
    dir("${WORKSPACE}/${BUILD_NUMBER}"){ 
    sh '''echo "localhost" > hosts'''
    } } }
stage("Executing scripts"){
steps {
dir("${WORKSPACE}/"){
sh '/usr/bin/ansible-playbook "${BUILD_NUMBER}"/test.yaml'
}}}
}}
