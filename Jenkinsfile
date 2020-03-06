pipeline {
    agent  { docker { image 'node' } }
    stages {
        stage('Build') {
            steps {
                bat 'ng build --prod --aot --sm --progress=false'
            }
        }
    }
}
