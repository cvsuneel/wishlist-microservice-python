#! groovy
node {
    stage('code') {
        
        sh " git branch: 'main', url: 'https://github.com/cvsuneel/wishlist-microservice-python.git' "
    }
    stage('Build') {
        sh 'docker build -t wishlist .'
    }
    stage('Deploy') {
        sh 'docker run -d -p 1003:1003 --restart unless-stopped --name wishlist wishlist'
    }
}
