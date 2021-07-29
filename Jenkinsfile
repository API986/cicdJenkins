pipeline {
agent any
stages {
stage('Build Application') {
steps {
bat 'mvn clean install'
}
}
stage('Deploy OnPremise') {
steps {
echo 'Deploying mule project due to the latest code commit….'
echo 'Deploying to the configured environment….'
bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=4.3.0 -Danypoint.username=NileshApi986 -Danypoint.password=Dhonil@698 -Dtarget=TPH-MULE-DEV -Dtarget.type=server -Denv=Development -Dappname=cicd-test-app3'
}
}
}
}