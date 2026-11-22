
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Timetable...'
                bat 'if exist index.html (if exist styles.css (echo Files Found)) else (exit /b 1)'
            }
        }

        stage('Test') {
            steps {
                bat 'findstr /C:"Weekly College Timetable" index.html'
                echo 'Tests Passed!'
            }
        }
    }
}
