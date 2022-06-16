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
dir("${WORKSPACE}/${BUILD_NUMBER}"){
sh '/usr/bin/ansible-playbook test.yaml'
}}}
}}
