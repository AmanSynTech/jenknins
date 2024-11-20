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
    stages {
        stage('Run Install Packages') {
            steps {
                echo "Installing required packages..."
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/2_InstallPackages
                    make
                '''
            }
        }
    }
}

