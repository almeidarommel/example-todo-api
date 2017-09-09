node('php'){
    stage('Clean'){
        deleteDir()
        sh 'ls -la'
    }
    
    stage('Fetch') {
        checkout scm
    }
    
    stage('Build'){
        sh 'composer install --prefer-dist --no-dev --ignore-platform-reqs'
        sh 'php artisan config:cache'
        // sh 'php artisan route:cache'
    }
    
//    stage('Docker Build') {
//        sh 'sudo docker build -t rommelalmeida/todoapi:$BUILD_NUMBER .'
//    }
    
//    stage('Docker Ship') {
//        sh 'sudo docker push rommelalmeida/todoapi:$BUILD_NUMBER'
//    }
}
