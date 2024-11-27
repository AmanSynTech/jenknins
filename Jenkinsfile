pipeline {
    agent any
    stages {
        stage('Running Base Ubuntu') {
            steps {
                echo "Creating ubuntu as base..."
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/1_BaseUbuntu
                    make
                '''
            }
        }
        stage('Running Install Packages') {
            steps {
                echo "*** Installing all the required packages ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/2_InstallPackages
                    make
                '''
            }
        }
        stage('Running Install SDK') {
            steps {
                echo "*** Installing SDK ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/3_InstallSDK
                    make
                '''
            }
        }
        stage('Running Create Emulator') {
            steps {
                echo "*** Creating required Emulator ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/4_CreateEmulator
                    make
                '''
            }
        }
        stage('Running Install Netbeans') {
            steps {
                echo "*** Installing required Netbeans App ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/5_InstallNetbeans
                    make
                '''
            }
        }
        stage('Running Install inventory Server') {
            steps {
                echo "*** Installing required Inventory Server ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/6_InstallInvServer
                    make
                '''
            }
        }
        stage('Building Scripts nad Installing App for Automation') {
            steps {
                echo "*** Building all the automation test scripts and installing app for headless testing ***"
                sh '''
                    cd /home/aman/inventory-testing-clone/DockerBuild/7_RunScript
                    make
                '''
            }
        }
    }
}

