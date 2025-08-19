pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/singh5277/fake-store-api-automation.git'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'newman run FakeStore_API_Testing.postman_collection.json'
            }
        }
    }
}
