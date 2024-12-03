pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/srk-ullagallu/testing.git'
            }
        }
        stage('Display Runner Information') {
            steps {
                sh '''
                echo "OS Information:"
                uname -a
                echo "Disk Space:"
                df -h
                echo "Memory Info:"
                free -h
                echo "Hello World"
                '''
            }
        }
        stage('Check Software Versions') {
            steps {
                sh '''
                echo "Checking installed software versions..."
                node -v || echo "Node.js not installed"
                npm -v || echo "NPM not installed"
                python3 --version || echo "Python not installed"
                pip --version || echo "Pip not installed"
                java --version || echo "Java not installed"
                mvn --version || echo "Maven not installed"
                git --version || echo "Git not installed"
                docker --version || echo "Docker not installed"
                docker-compose --version || echo "Docker Compose not installed"
                ansible --version || echo "Ansible not installed"
                terraform --version || echo "Terraform not installed"
                packer --version || echo "Packer not installed"
                aws --version || echo "AWS CLI not installed"
                kubectl version --client || echo "Kubectl not installed"
                trivy --version || echo "Trivy not installed"
                k9s version || echo "K9s not installed"
                dotnet --version || echo "Dotnet not installed"
                tfsec --version || echo "TFSEC not installed"
                sonar-scanner --version || echo "Sonar Scanner not installed"
                echo "All the above packages have been checked."
                '''
            }
        }
    }
}
