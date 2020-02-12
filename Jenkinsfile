pipeline {
    agent  { docker { image 'node:10' } }
    stages {
        stage('Build') {
            steps {
                bat 'ng build --prod --aot --sm --progress=false'
            }
        }
    }
}
