pipeline {
    agent any
    stages {
        stage('Credentials') {
            environment {
                SECRET_VALUE = credentials('dbdevops')
            }
            steps {
                sh 'bash  $JENKINS_HOME/Flyway-test-31/flyway -locations=filesystem:db/Version1.1/sql -baselineVersion=1.0 --url=jdbc:postgresql://devopstestdb.chzkxi0lcrpk.ap-south-1.rds.amazonaws.com:5432/example --driver=org.postgresql.Driver --classpath=$JENKINS_HOME/Flyway-test-31/drivers/postgresql-42.2.23.jar -user=$SECRET_VALUE_USR -password=$SECRET_VALUE_PSW $option'
            }
        }        
    }
}
