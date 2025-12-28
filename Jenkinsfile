pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/krsaeed/Hello_World_py.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                pip3 install -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                nohup python3 app.py &
                '''
            }
        }
    }
}
