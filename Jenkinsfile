
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Timetable...'
                sh 'test -f index.html && test -f styles.css'
            }
        }

        stage('Test') {
            steps {
                sh 'grep -q "Weekly College Timetable" index.html'
                echo 'Tests Passed!'
            }
        }
    }
}
