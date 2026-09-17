pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/niha1526/student-management-project2.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat '''
                echo Student Management and Academic Performance System > report.txt
                echo Total Students: 120 >> report.txt
                echo Active Students: 95 >> report.txt
                '''
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
