pipeline {
    agent any

    stages {
        stage('CompileJob') {
            steps {
		echo 'code validate'
		sh 'mvn validate'
            }
        }
        stage('UnitTest') {
            steps {
		echo 'code test'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
		 echo 'code analysis'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://65.2.144.136:9000/-Dsonar.login=a65dcdbd635a68c377369ef5222f3da351007981'
            }
        }
    }
}
