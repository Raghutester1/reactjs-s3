pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
                // sh 'ls'
                // sh 'cd build'
                // sh 'ls'
                sh '''
                    echo "Listing only files in the build directory:"
                    find build/ -type f
                '''
            }
        }
        // stage('S3 Upload') {
        //     steps {
        //         withAWS(region: 'us-east-2', credentials: 'access_keys') {
        //             sh 'ls -la build'
        //             sh 'aws s3 cp build s3://jenkins-react-sk/ --recursive'
        //         }
        //     }
        // }
    }
}
