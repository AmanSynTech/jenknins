pipeline {
    agent any
    stages {
        stage('Run Base Ubuntu') {
            steps {
                echo "Creating ubuntu as base..."
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/1_BaseUbuntu
                    make
                '''
            }
        }
    }
    
}

