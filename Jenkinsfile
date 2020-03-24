pipeline {
    agent  { 'Node Apps' }
    stages {
        stage('Build') {
            steps {
                bat 'ng build --prod --aot --sm --progress=false'
            }
        }
    }
}
